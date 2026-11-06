# instabox-danh-thuc

GitHub Actions cứ 7 tiếng một lần đánh thức box instabox (`chatbot`) nếu nó đang dừng, rồi kiểm tra service bot (`trolybaogia`) còn chạy không, chết thì bật lại.

- Box tự tạm dừng thì được đánh thức, tiến trình chạy tiếp từ chỗ cũ. Box bị tắt hẳn thì được bật lại, systemd tự mở bot.
- Box đang trong thời gian chờ của instabox thì lần đó bỏ qua.
- Chạy tay: tab **Actions** → **Danh thuc box instabox** → **Run workflow**.

Cần secret `INSTABOX_API_KEY` (tạo ở dashboard instabox, mục API keys). Đổi box/service bằng biến `BOX_NAME`, `SERVICE_NAME` trong Settings → Variables.

GitHub tự tắt lịch chạy nếu repo không có commit nào trong 60 ngày; khi đó vào tab Actions bật lại.
