---
title: Triển khai container service
weight: 3
---

# Triển khai container service

Khi project đã tồn tại, luồng chính thường là tạo deployment service từ external image hoặc output build của Northflank.

## Các đầu vào khi triển khai

Màn hình tạo service chia cấu hình thành các nhóm thực tế:

![Biểu mẫu deployment service trên Northflank](/images/northflank-deploy-service.png)

- danh tính service
- nguồn image
- compute plan
- mở port
- biến môi trường
- hành vi runtime nâng cao

## Một mental model hữu ích

Northflank yêu cầu bạn mô tả workload theo đúng thứ tự mà người vận hành nghĩ về production:

{{% steps %}}

### Đặt tên service

Dùng tên ổn định vì nó xuất hiện trong URL, log và lịch sử deployment.

### Chọn nguồn image

Chọn external image khi bạn đã publish image lên Docker Hub hoặc registry khác.

### Thiết lập compute và storage

Ghép CPU, RAM, ephemeral storage và số instance với nhu cầu nền của workload.

### Cấu hình networking

Chỉ public các port thực sự cần truy cập và giữ phần còn lại ở private.

### Thêm runtime configuration

Chỉ bơm biến môi trường, health check và command behavior sau khi định nghĩa service đã ổn định.

{{% /steps %}}

{{< details title="Những gì cần kiểm tra trước khi bấm create" >}}

- Đúng image tag
- Đúng public/private exposure
- Đúng port và protocol
- Mức CPU/RAM tối thiểu phù hợp
- Đủ runtime variables bắt buộc

{{< /details >}}
