# FrogNutri – GitHub Pages + Supabase

Bộ website FrogNutri hoàn chỉnh theo Master Prompt: trang chủ, câu chuyện, dinh dưỡng/kiểm nghiệm, nghiên cứu, shop, chi tiết sản phẩm, giỏ hàng, review + upload ảnh, tài khoản, chatbot FAQ và responsive.

## Kết nối database thật
1. Tạo project Supabase.
2. Mở SQL Editor và chạy `supabase/schema.sql`.
3. Project Settings → API: lấy Project URL và Publishable/anon key.
4. Điền vào `js/config.js`.
5. Auth → URL Configuration: đặt Site URL là URL GitHub Pages và thêm Redirect URL tương ứng.
6. Đẩy thư mục lên GitHub → Settings → Pages → Deploy from branch.

Không đưa `service_role` key vào frontend/GitHub.

## Giá
Master Prompt không cung cấp giá chính thức hiện tại nên `js/data.js` để `price:null`. Khi có giá thật, sửa tại đó.

## PDF/ảnh
Ảnh đặt trong `assets/images/`; PDF kiểm nghiệm thật đặt trong `assets/documents/`. Không tạo tài liệu giả.

## Chạy local
Có thể dùng VS Code Live Server để test. Bản chính thức chạy trên GitHub Pages.

## Tính năng thật sau khi cấu hình Supabase
- Email/password Auth
- Profile
- Session persistence
- Lịch sử đơn hàng
- Review database
- Upload ảnh review vào Storage
- RLS bảo vệ dữ liệu người dùng

## Tính năng frontend/demo
- Giỏ hàng lưu localStorage
- Chatbot hiện là FAQ, không giả vờ là AI API
- Giá sản phẩm chưa nhập nên chưa thể tạo đơn có giá thật
