# VIG PixOptimizer

**Nén & tối ưu ảnh cho web — giảm dung lượng tới ~80% mà chất lượng gần như nguyên vẹn.**
Kéo ảnh vào, nhận ảnh nhẹ hơn (JPG · PNG · WebP) để trang tải nhanh, tốt cho SEO.

▶ **Dùng ngay:** https://tools.vigdigital.com/pixoptimizer/

## ✨ Tính năng
- Nén mạnh bằng codec chuẩn công nghiệp **MozJPEG** + **WebP** (WASM)
- Chế độ **Tự động**: thử WebP và định dạng gốc, chọn bản nhỏ nhất
- **Thu nhỏ** ảnh quá khổ (mặc định ≤ 2000px) như plugin VIG Image Optimizer
- **So sánh trước/sau** bằng slider; tải 1 ảnh hoặc cả bộ `.zip`
- Xử lý nhiều ảnh; có giới hạn để không làm treo trình duyệt (20 ảnh · ≤25MB/ảnh · ≤100MB/lượt)
- **Không phụ thuộc CDN ngoài**: codec self-host (bundle + .wasm cạnh file)

## 🎯 Vì sao có tool này
Demo cho khách trải nghiệm **kết quả tối ưu ảnh** của VIG. Muốn tự động hoá cho cả
website WordPress (nén khi upload, xử lý hàng loạt, tự chuyển WebP) → dùng **plugin
VIG Image Optimizer**. Tool này là "nếm thử", plugin là bản tự động + hàng loạt.

## 🛠️ Build codec (khi cập nhật jSquash)
```bash
cd build
npm i
npx esbuild entry.js --bundle --format=esm --outdir=../assets/codecs --entry-names=codecs
# copy .wasm cạnh bundle (mozjpeg_enc / webp_enc / webp_enc_simd)
```
Chi tiết deploy hạ tầng: doc nội bộ `Hosting/tools.vigdigital.com.md` (không đưa vào repo public).

## 📄 Giấy phép & nguồn
- Mã nguồn: **MIT** (xem `LICENSE`) — dùng lại tự do, vui lòng **giữ dòng ghi nguồn VIG Digital**.
- Ghi nguồn có ở: comment đầu `index.html` (view-source), `<meta author/generator>`, banner console (inspect), footer trang.
- Ảnh mẫu (`assets/sample.jpg`): ảnh của **r. nolan / Unsplash** (Unsplash License).

Made with ♥ by [VIG Digital](https://vigdigital.com).
