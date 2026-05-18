---
title: Tổng quan nền tảng
weight: 1
---

# Tổng quan nền tảng

Northflank được tổ chức quanh vài thực thể cốt lõi. Khi hiểu chúng, phần còn lại của sản phẩm sẽ dễ điều hướng hơn nhiều.

## Các khối nền tảng

{{< cards cols="2" >}}
  {{< card title="Team" icon="users" subtitle="Workspace dùng chung cho thành viên, billing, integrations và quyền sở hữu project." >}}
  {{< card title="Project" icon="cube-transparent" subtitle="Ranh giới gom workload, networking, secrets và environments." >}}
  {{< card title="Service" icon="server" subtitle="Workload container chạy dài hạn, có thể public hoặc private." >}}
  {{< card title="Job" icon="clock" subtitle="Tác vụ container chạy một lần hoặc theo lịch cho script, worker và automation." >}}
{{< /cards >}}

## Dashboard đang nói gì

Ảnh dashboard cho thấy quan điểm sản phẩm khá rõ: Northflank muốn bạn bắt đầu bằng project, rồi thêm đúng các runtime component cần cho project đó.

![Tổng quan dashboard Northflank](/images/northflank-dashboard.png)

{{< details title="Các loại tài nguyên phổ biến trong project" >}}

- Build service cho CI/container build
- Deployment service để chạy image
- Job cho tác vụ thủ công hoặc theo lịch
- Volume cho lưu trữ bền vững
- Add-on cho dependency trạng thái
- Secret group và environment cho cấu hình

{{< /details >}}

## Cách đọc mô hình nền tảng

{{% steps %}}

### Nghĩ theo team trước

Team sở hữu quyền truy cập, thành viên, integrations và billing.

### Nghĩ theo project tiếp theo

Project là container chính cho các tài nguyên ở cấp ứng dụng.

### Nghĩ theo runtime sau cùng

Service, job, port, biến môi trường và health check đều được cấu hình bên trong project chứa workload.

{{% /steps %}}

![Menu tạo tài nguyên trên Northflank](/images/northflank-resource-menu.png)
