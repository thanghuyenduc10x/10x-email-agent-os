# CLAUDE.md — 10x-email-agent-os

## Repo này là gì

Hồ sơ public của **10X Email Agent V1**, golden case của Agent Publishing OS: tri thức gốc, manifest, website tĩnh, quy trình publish và QA.

Repo **không** chứa agent chạy thật. Agent hiện chạy trong ChatGPT (kết nối Gmail, theo Quick Start). Runtime 24/7 dự kiến là Hermes trên VPS, nằm ở repo private `agent-hermes-vps`.

## Nguồn sự thật

| Nội dung | File |
| --- | --- |
| Tri thức Email Agent (P0–P5, nhãn, lịch, an toàn, test) | `knowledge/EMAIL-AGENT-CANONICAL-V1.md` |
| Dữ liệu cấu trúc | `agent.yaml` |
| Spec và Definition of Done V1 (LOCKED, chỉ sửa khi Coach duyệt) | `AGENT-PUBLISHING-OS-V1-SPEC.md` |
| Website | `website/` |
| Bằng chứng nghiệm thu | `qa/` |

Thứ tự sửa: canonical → `agent.yaml` → `website/`. Website không được có nội dung mà canonical không có.

Khi được yêu cầu `Public Agent`, `publish agent`, `push GitHub` hoặc `publish website`: làm theo `skills/publish-agent/SKILL.md` và `instructions/PUBLIC-AGENT-WORKFLOW.md`.

## Deploy

- Merge vào `main` có thay đổi trong `website/**` hoặc file workflow → `.github/workflows/deploy-pages.yml` đăng lên GitHub Pages. Thay đổi ngoài `website/` không kích hoạt deploy.
- Production: https://agent-email.10x-lifeos.com/ (`website/CNAME`; DNS ở Hostinger trỏ CNAME về `thanghuyenduc10x.github.io`).
- Không đổi domain/CNAME, visibility của repo hay cài đặt Pages khi chưa được yêu cầu rõ.

## Kiểm tra trước khi push

Không có bước build hay bộ test tự động. Với thay đổi trong `website/`:

- Đủ 7 section: Problem, Destination, System, Roadmap, Quick Start, Test & Definition of Done, Evolution.
- Mobile 390 px không tràn ngang; console trình duyệt không lỗi.
- Link nội bộ và asset đều tồn tại.

## An toàn — repo PUBLIC

- Không commit secret, token, nội dung email thật, dữ liệu khách hàng/học viên hay số tài khoản. Ví dụ và test chỉ dùng email giả lập.
- Không báo push/deploy/domain thành công khi chưa có bằng chứng từ tool (run GitHub Actions thành công, HTTP 200).

## Việc đang mở

- Kế hoạch Gmail trong `agent-hermes-vps` dùng lịch quét và lịch brief khác canonical ở đây. Chưa quyết bản nào là chuẩn.
- `10X-LifeOS` coi `09_KNOWLEDGE_BASE` là Canon duy nhất, nhưng tri thức Email Agent hiện chỉ nằm ở repo này, chưa được liên kết vào Canon.
