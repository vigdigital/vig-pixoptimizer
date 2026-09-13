# Roadmap — VIG PixOptimizer

## Ưu tiên cao
1. **AVIF** (nén tốt hơn WebP ~20-30%) — thêm codec @jsquash/avif; nặng hơn, cân nhắc lazy.
2. **Ảnh mẫu thật** thay ảnh plasma tổng hợp (demo % thực tế, đáng tin hơn).
3. **Nén theo dung lượng mục tiêu** (vd "≤ 200KB") thay vì chỉ theo quality.

## Cân nhắc
4. Giữ tỉ lệ % theo từng ảnh trong bảng tổng; sort theo mức giảm.
5. PNG lossless mạnh hơn (oxipng) — cần bản non-parallel để tránh COOP/COEP.
6. Kéo-thả cả thư mục; nhớ tuỳ chọn lần trước (localStorage).

## Đã chốt
- Client-side 100%, codec self-host (không CDN ngoài).
- Bỏ oxipng bản parallel (cần SharedArrayBuffer/COOP-COEP) — PNG nén mạnh nhất = chuyển WebP.
