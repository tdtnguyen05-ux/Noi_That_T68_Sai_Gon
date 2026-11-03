# NỘI THẤT T68 SÀI GÒN

Website tĩnh nhiều trang, tông trắng kem – xanh navy – vàng đồng. Có trang chủ, giới thiệu, danh mục, mẫu nội thất, dịch vụ, ý tưởng không gian, cẩm nang, liên hệ, FAQ, bảo mật, điều khoản và sơ đồ website.

## Trạng thái bàn giao — 02/11/2026

- 127 tệp HTML: 126 địa chỉ nội dung, cộng tệp lỗi `404.html` ở gốc.
- 42 mẫu nội thất, 8 nhóm không gian, 15 nhóm sản phẩm, 8 hướng dịch vụ, 30 bài ý tưởng không gian, 10 bài cẩm nang.
- **39 ảnh WebP riêng biệt đã tạo và kiểm chứng**, chưa đạt mục tiêu 120 ảnh. Hạn mức tạo ảnh đã hết; 81 yêu cầu ảnh còn lại được ghi rõ trong `data/image-briefs.json`. Không có tệp giả hoặc nhân bản để tăng số lượng. Một số trang dùng chung hình cảm hứng.
- Font đóng gói: **Noto Serif, Noto Sans, Carlito**, có ký tự tiếng Việt. Chưa phải Playfair Display, Montserrat, Be Vietnam Pro trong đề bài vì nguồn tải bị chặn. Cả website và bản HTML offline dùng cùng bộ font này để giữ nhất quán.
- Chưa có dữ liệu doanh nghiệp được xác nhận: điện thoại, email, địa chỉ, thông tin thương mại, giá, vật liệu thực tế và chính sách bảo hành. Không tạo số liệu giả. Biểu mẫu mặc định **tải phiếu về máy**, chưa gửi tới doanh nghiệp.
- Chưa đưa mã lên GitHub, chưa bật Pages. Đây là gói xuất bản, không phải xác nhận website đã online.
- Đã kiểm tra cấu trúc, ảnh, liên kết, cú pháp JavaScript và phục vụ HTTP dưới thư mục dự án. **Chưa chạy thử tương tác trong trình duyệt, chưa kiểm chứng responsive bằng ảnh chụp, chưa đo Lighthouse** do môi trường không có trình duyệt và chặn tải. Xem `docs/BAO_CAO_KIEM_THU.md`.

## Xuất bản lên GitHub Pages

Repository: https://github.com/tdtnguyen05-ux/Noi_That_T68_Sai_Gon

1. Giải nén `Noi_That_T68_Sai_Gon_Full_Website.zip`.
2. Đưa **nội dung bên trong ZIP** vào gốc repository, nhánh `main`. Tệp `index.html`, thư mục `assets`, `data`, cùng các thư mục trang phải nằm cùng cấp. Không tải nguyên tệp ZIP để làm website và không lồng thêm thư mục.
3. Giữ tệp `.nojekyll` ở gốc. Nếu tải bằng giao diện GitHub, kiểm tra cả tệp này đã được thêm.
4. Mở **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
5. Chọn **main** và **/(root)**, bấm **Save**.
6. Chờ công việc Pages hoàn tất trong Actions, rồi mở https://tdtnguyen05-ux.github.io/Noi_That_T68_Sai_Gon/ . Kiểm tra lại các luồng thực tế trước khi giới thiệu website công khai.

Không cần npm, Node server, PHP hoặc build để xuất bản bản đã đóng gói. Cần quyền quản trị/duy trì phù hợp để cấu hình Pages. Hướng dẫn GitHub chính thức: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Bản HTML độc lập

`Noi_That_T68_Sai_Gon_Preview_All_In_One.html` là tệp bàn giao riêng. Mở bằng trình duyệt, có thể tắt mạng. Ảnh, font, CSS, JavaScript và 126 màn nội dung được nhúng bên trong. Điều hướng dùng hash `#/san-pham/` thay vì URL thư mục. Giao diện và nội dung sinh từ cùng nguồn với website.

Tính năng cần mạng chỉ xuất hiện khi bổ sung kênh email/dịch vụ nhận biểu mẫu. Chia sẻ dùng địa chỉ web dự kiến, chỉ truy cập được sau khi xuất bản. Trình duyệt có thể hạn chế bộ nhớ cục bộ khi mở file; khi đó danh sách yêu thích chỉ giữ trong phiên.

## Cập nhật

Xem `docs/HUONG_DAN_CAP_NHAT.md`. Dữ liệu nằm trong `data/*.json`, giao diện trong `assets/css/`, hành vi trong `assets/js/main.js`, mẫu trang và bộ xuất bản trong `tools/build.py`.

Sau khi sửa dữ liệu hoặc mẫu trang, chạy với Python 3:

```bash
python tools/build.py ../deliverables
```

Lệnh tái tạo HTML, dữ liệu nhúng cho trình duyệt, sitemap, ZIP và HTML offline. Python chỉ cần khi cập nhật, không cần để hiển thị hoặc xuất bản. Tải toàn bộ đầu ra website đã tái tạo lên repository. Không chỉ sửa `brand.json` rồi bỏ qua bước tái tạo.

Đề xuất mô tả repository: “Website Nội Thất T68 Sài Gòn – Thiết kế, thi công, tư vấn và giải pháp nội thất hiện đại, sang trọng, tối ưu trải nghiệm người dùng.”
