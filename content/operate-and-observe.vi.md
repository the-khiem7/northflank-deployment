---
title: Vận hành và quan sát
weight: 4
---

# Vận hành và quan sát

Deploy chỉ là điểm giữa. Màn hình tổng quan service chứa các công cụ bạn dùng sau khi launch để chứng minh workload đang khỏe.

## Các bề mặt runtime nên học

{{< cards cols="2" >}}
  {{< card title="Deployments" icon="refresh" subtitle="Xem lịch sử rollout, image hiện tại và mốc thời gian sự kiện." >}}
  {{< card title="Logs" icon="terminal" subtitle="Mở runtime logs để chẩn đoán lỗi boot và lỗi ứng dụng." >}}
  {{< card title="Metrics" icon="chart-square-bar" subtitle="Theo dõi CPU, RAM và xu hướng hành vi qua từng revision." >}}
  {{< card title="Command override" icon="pencil" subtitle="Điều chỉnh startup behavior mà chưa cần rebuild image ngay." >}}
{{< /cards >}}

![Màn hình runtime overview của service trên Northflank](/images/northflank-runtime.png)

## Checklist sau deploy

{{% steps %}}

### Xác nhận image và revision

Đảm bảo deployment đang chạy đúng tag hoặc release bạn dự kiến.

### Xem log khởi động

Phát hiện sớm biến môi trường sai, port sai, migration lỗi hoặc dependency chưa sẵn sàng.

### Kiểm tra networking

Mở URL service được tạo và xác nhận port mong đợi có thể truy cập.

### Theo dõi độ ổn định

Kiểm tra restarts, deployment events và mức bão hòa tài nguyên trước khi xem rollout là hoàn tất.

{{% /steps %}}
