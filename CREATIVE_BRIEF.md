# Creative brief

## Mục tiêu
Tái tạo trang web thành một nơi để cảm ơn mọi người và kỷ niệm những khoảnh khắc đã cùng nhau trải qua.

## Phạm vi
- Làm lại từ đầu các phần nội dung hiện có, ngoại trừ những phần bắt buộc phải giữ.
- Khi mở website, màn hình đầu tiên có giao diện với một hình ảnh rất lớn và hai lựa chọn: vào menu chính hoặc điền thông tin.
- Bắt buộc giữ phần Home ở màn hình đầu, bao gồm nút vào menu chính.
- Bắt buộc giữ lựa chọn/luồng điền thông tin (Applications/đăng ký), vì mọi người vẫn cần truy cập.
- Nhấn nút vào menu chính sẽ dẫn tới giao diện web kỷ niệm.
- Giao diện kỷ niệm sử dụng phong cách Parallax.
- Giữ nguyên giao diện/nhận diện hiện tại của website, bao gồm font chữ, màu chữ và phong cách tổng thể. Không thay đổi ngôn ngữ hình ảnh hiện có khi tái tạo các phần kỷ niệm.
- Trải nghiệm kỷ niệm được cá nhân hóa qua mã QR riêng cho từng học sinh: khi quét, website nhận diện học sinh và hiển thị trang của bạn ấy với tên, lời cảm ơn và ảnh.
- Trang QR mở trực tiếp, không yêu cầu qua cổng truy cập quản trị hiện tại.
- Người xem chính là học sinh của cả Trường Trung Sơn và Trường Ngôi Sao Hoàng Mai.
- Giai đoạn đầu triển khai cả timeline chung và mẫu trang QR cá nhân; thông tin cá nhân thật sẽ bổ sung khi có danh sách học sinh.
- Mẫu QR dùng mã định danh `student` để tra hồ sơ trong `memories/profiles.js`; chỉ có hồ sơ demo cho tới khi có danh sách và ảnh được duyệt. Không đặt tên hay lời nhắn riêng trực tiếp lên URL.
- Mã `student=demo` chỉ dùng xem thử, không dùng làm QR thật; chưa tạo QR phát cho học sinh vì chưa có hồ sơ cá nhân đã được duyệt.

## Nội dung dòng thời gian
Kể lại hành trình của học sinh Trường Trung Sơn (Cao Hùng, Đài Loan) tại Việt Nam:
1. **Ngày 1–3 (19/10–21/10):** sang thăm Trường Ngôi Sao Hoàng Mai tại Hà Nội.
2. **Ngày 4:** vui chơi tại Vịnh Hạ Long.
3. **Ngày 5:** tham quan “Dinh Bác” và “Hồ Hoàng Kim” (cách gọi theo thông tin ban đầu; cần xác nhận tên địa điểm chính thức).
4. **Sân bay:** lưu lại khoảnh khắc của đoàn tại sân bay; thời điểm cụ thể chưa nêu.

## Định hướng sáng tạo
- Trang web nên truyền tải sự biết ơn và lưu giữ kỷ niệm.
- Có thể dùng ảnh mẫu từ Internet trong bản dựng; thay bằng ảnh thật của đoàn sau.

## Quyết định hướng triển khai
- Trang kỷ niệm sẽ giữ hệ thống thị giác hiện có và kể chuyến giao lưu theo timeline Parallax, phục vụ học sinh hai trường.
- Mã QR mở thẳng trang cá nhân; trước khi có danh sách học sinh, chỉ dựng mẫu và không tự đặt tên/lời cảm ơn cá nhân như dữ kiện thật.
- Đã chọn cấu trúc “Những lớp ký ức”: mỗi hoạt động mở ra như một lớp ảnh Parallax, với phần timeline tiếp nối bên dưới.

## Direction contract — trang kỷ niệm

**THESIS:** Những lớp ký ức đưa học sinh hai trường đi lại hành trình giao lưu qua các cảnh ảnh Parallax; từ chối bố cục landing page chung chung.

**OWN-WORLD:** Giữ giấy ngà `#f1efe9`, mực `#191b1b`, đất nung `#a24f38`, xanh `#334f60`, font DM Sans / Space Grotesk / DM Mono và nét mảnh đang dùng trên MIYO.

**STORY:** Người xem bước vào hành trình chung, cuộn qua từng chặng và có thể mở trang QR cá nhân; ảnh mẫu được nhận diện là minh họa, không giả làm ảnh đoàn thật.

**FIRST VIEWPORT:** Ảnh nhóm bạn minh họa tràn khung; tiêu đề “Những ngày thân quen.” đặt lớn phía dưới-trái; đường nét nối Hà Nội–Cao Hùng nằm trên ảnh như dấu hiệu MIYO; mép dưới dẫn vào timeline.

**FORM:** Trải nghiệm / thứ hạng grounded 4; cấu trúc “những lớp ký ức”: ảnh Parallax, vệt kết nối MIYO, thanh tiến độ cuộn và một cảnh Vịnh Hạ Long toàn khung làm điểm nhấn; seed:736ef8c4b657f5cb.

**FINISH:** unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
