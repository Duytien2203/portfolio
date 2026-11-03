# DESIGN.md - Design System & Visual Language

## 1. Triết Lý Thiết Kế (Aesthetic Direction)
* **Vibe:** Deep Midnight, Ambient Soft Glass & Organic Fluidity (High-Tech, Refined, Soft & Tactile Dark Theme).
* **Bản chất màu sắc & Ánh sáng môi trường (Midnight & Ambient Synergy):**
  * **Sắc Đen Chiều Sâu (Deep Midnight Canvas `#070a12`):** Tạo phông nền vô cực, hiện đại, phối hợp cùng các quầng sáng môi trường mềm mại (ambient diffuse glow orbs: Emerald & Cyan 5-8% opacity) giúp trang không bị cứng hay tạo cảm giác hộp đóng kín.
  * **Sắc Ngọc Lục Bảo (Emerald `#10b981` & `#34d399`):** Chuẩn mực, tăng trưởng bền vững (growth), độ tin cậy và sự chính xác.
  * **Sắc Cyan & Electric Sky (`#06b6d4` & `#38bdf8`):** Công nghệ dữ liệu, Machine Learning và tính năng động.
* **Cải tiến độ mềm & mượt (Soft & Fluid Polish):**
  * **Góc bo tự nhiên (Harmonic Radii):** Thẻ dự án chính nâng cấp lên `rounded-3xl` (24px) tạo hình khối mềm mại như đá cuội hữu cơ. Các khung bên trong dùng `rounded-2xl` và `rounded-xl`.
  * **Kính mờ đa tầng (Soft Glassmorphism):** Thẻ `.glass-panel` ứng dụng gradient mờ nhẹ `rgba(16, 24, 40, 0.72) -> rgba(11, 16, 28, 0.82)`, `backdrop-filter: blur(16px)` cùng đường gờ satin `inset 0 1px 0 rgba(255, 255, 255, 0.06)`.
  * **Chuyển động mượt mà (Fluid Timing Curve):** Toàn bộ tương tác hover dùng đường cong gia tốc tự nhiên `cubic-bezier(0.16, 1, 0.3, 1)` với độ nâng `-3px` và bóng đổ sâu trung tính.
  * **Thanh Filter dạng Soft Pills:** Chuyển các tab lọc dự án sang dạng viên thuốc `rounded-full` mượt mà, tab active đổ bóng trung tính nhẹ nhàng.
  * **Cuộn trang mượt mà:** Bật `scroll-behavior: smooth` trên toàn trang.

## 2. Bảng Màu Chuẩn (Color Tokens)
* **Background Root:** `#070a12` (Midnight Deep Canvas)
* **Section Canvas:** `#0b101c` (Midnight Base) & `#101726` (Midnight Card Surface)
* **Card Surface:** `linear-gradient(145deg, rgba(16, 24, 40, 0.72) 0%, rgba(11, 16, 28, 0.82) 100%)` với viền `rgba(255, 255, 255, 0.08)`, bóng đổ đa tầng trung tính `0 10px 30px -10px rgba(0, 0, 0, 0.45)`.
* **Card Hover:** `transform: translateY(-3px)`, viền `rgba(52, 211, 153, 0.32)`, bóng mở rộng `0 20px 40px -15px rgba(0, 0, 0, 0.7)`.
* **Primary Accent:** `from-emerald-500 to-cyan-500 text-midnight-950 font-bold`.
* **Typography Roles (Độ Tương Phản Chuẩn WCAG AAA / AA):**
  * `Heading / Display`: `#ffffff` (Pure White sắc nét).
  * `Body Text`: `#cbd5e1` (Slate 300 êm mắt, dễ chịu).
  * `Accent Highlights`: `#34d399` (Emerald 400) & `#38bdf8` (Cyan 400).
* **Badge & Pill System:**
  * Dạng viên thuốc `rounded-full` nhẹ nhàng: `bg-emerald-500/10 text-emerald-300 border border-emerald-500/20`.
  * `Badge Cyan`: `bg-cyan-500/10 text-cyan-300 border border-cyan-500/20`.
  * `Badge Amber`: `bg-amber-500/10 text-amber-300 border border-amber-500/20`.

## 3. Hệ Thống Kiểu Chữ (Typography Scale)
* **Font chữ tiêu đề & nội dung:** `Be Vietnam Pro` (400, 500, 600, 700, 800) – hỗ trợ tiếng Việt sắc nét.
* **Font chữ số liệu & mã nguồn:** `JetBrains Mono` – khoa học, chuẩn xác cho DOI và chỉ số.
* **Quy tắc phân cấp:**
  * Hero Display: `clamp(2rem, 4vw, 3.25rem)`, leading 1.18, tracking `-0.025em`.
  * Section Title: `clamp(1.5rem, 3vw, 2.25rem)`, leading 1.25, tracking `-0.02em`.
  * Card Heading: `clamp(1.15rem, 2vw, 1.5rem)`, leading 1.35.

## 4. Tương Tác & Chi Tiết Hoàn Thiện (Micro-Craft)
* **Filter Tabs Bar:** Dạng viên thuốc `rounded-full`, hiệu ứng chuyển đổi tab êm ái với `cubic-bezier(0.16, 1, 0.3, 1)`.
* **Slide Preview Frames:** Khung chiếu slide viền mảnh, bo góc êm ái, dải thumbnail nhấp chuột đổi slide tức thì kèm phản hồi viền sáng.
* **Theater Lightbox Modal:** Áp dụng `backdrop-blur-xl` mềm mại cùng phông nền `rgba(7, 10, 18, 0.90)`.
