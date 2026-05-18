---
title: Thiết lập team và project
weight: 2
---

# Thiết lập team và project

Luồng đầu tiên trên Northflank không chỉ là deploy, mà còn là tạo đúng workspace ngay từ đầu.

## Những gì diễn ra trước tiên

Các màn hình onboarding cho thấy ba hành động sớm:

![Biểu mẫu onboarding của Northflank](/images/northflank-onboarding.png)

- xác nhận thông tin tài khoản
- tạo hoặc tham gia team
- chọn project đầu tiên cùng dạng plan

## Vì sao việc này quan trọng

Thiết lập team ảnh hưởng trực tiếp tới cách bạn mời cộng tác viên, kết nối Git provider và tách project về sau.

![Thiết lập team và plan trên Northflank](/images/northflank-team-setup.png)

{{% steps %}}

### Hoàn tất onboarding

Điền thông tin tài khoản cơ bản và chấp nhận các điều khoản bắt buộc của nền tảng.

### Tạo team

Đặt tên workspace rõ ràng vì nó sẽ là container cho các project và thành viên trong tương lai.

### Chọn plan khởi đầu

Dùng free hoặc starter để xác thực workflow, rồi mở rộng khi giới hạn tài nguyên trở thành vấn đề thực tế.

### Tạo project đầu tiên

Chọn deployment target và region dựa trên nơi workload cần chạy và mức độ kiểm soát hạ tầng bạn muốn có.

{{% /steps %}}

![Chọn region cho project trên Northflank](/images/northflank-region.png)

{{< callout type="warning" >}}
Việc chọn region ảnh hưởng tới latency, plan khả dụng và đôi khi cả GPU availability. Hãy xem đây là quyết định vận hành, không chỉ là một ô biểu mẫu.
{{< /callout >}}
