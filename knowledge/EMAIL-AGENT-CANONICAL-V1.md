# 10X Email Agent — Canonical V1

## Problem
Inbox lộn xộn, email quan trọng lẫn newsletter/promotion, người dùng phải tự kiểm tra nhiều lần và có nguy cơ bỏ sót thanh toán, bảo mật, quyền truy cập, cộng sự và deadline.

## Destination
AI đọc và phân loại email, cảnh báo P0 ngay, gửi Email Brief mỗi 2 giờ, Daily Digest cuối ngày và giữ con người ở vòng phê duyệt. Mục tiêu vận hành: giảm mạnh thời gian xử lý email, không tự gửi/xóa trong V1.

## Priority Model
- P0: Cần xử lý ngay.
- P1: Cần trả lời.
- P2: Cần theo dõi.
- P3: Thông tin cần biết.
- P4: Thông báo hệ thống.
- P5: Không quan trọng.

## Content Labels
Thanh toán & Hóa đơn; Cộng sự & Đối tác; Google Drive & Quyền truy cập; Vận hành hệ thống; Xác minh & Bảo mật; Newsletter & Promotion.

## Safety
Không tự gửi trả lời, không xóa; promotion chỉ archive sau giai đoạn kiểm định và chỉ khi độ tin cậy cao; email không chắc chắn giữ ở Inbox.

## V1 Build Journey
1. Tạo labels.
2. Pilot 100 email gần nhất.
3. Gắn nhãn thật 30 email đại diện.
4. Cảnh báo P0 tức thời.
5. Email Brief 08:00–20:00 mỗi 2 giờ.
6. Daily Digest 21:00.
7. Theo dõi ổn định 3 ngày.
8. Backfill an toàn sau gate kiểm định.

## Quick Start cho học viên
1. Kết nối Gmail với ChatGPT.
2. Tạo/kiểm tra bộ nhãn ưu tiên + nội dung.
3. Chạy pilot read-only trước khi sửa Inbox.
4. Test P0/P1/P3/P5 bằng email giả lập không nhạy cảm.
5. Chỉ bật archive promotion sau khi qua gate ổn định.

## Test Cases
- P0: thanh toán thất bại hoặc cảnh báo đăng nhập bất thường → phải cảnh báo ngay.
- P1: email người thật cần trả lời nhưng không khẩn → vào Brief, không ping P0.
- P3: mã xác minh thông thường hoặc hóa đơn đã thanh toán → ghi nhận, không P0.
- P5: newsletter/promotion → không chiếm phần quan trọng của Brief; chưa archive trong giai đoạn đầu.

## Evolution
V2: reusable template cho N Agent.
V3: AI distill/generate/publish từ conversation/Second Brain.
V4: 10X Agent Library quản lý catalog/version/status.
Perfection: Knowledge → Impact → Feedback → Second Brain learning loop.
