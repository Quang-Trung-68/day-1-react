# 🧠 React Practice Exercises

## 📁 Cấu trúc thư mục

```
/index.html
/rce.html
/jsx.html
/jsx-map.html
```

---

## 1️⃣ rce.html — React.createElement() Practice

### 🎯 Mục tiêu

Làm quen với React **mà không sử dụng JSX**.

### 🧩 Nội dung

- Tạo phần tử `#root` và render React elements bằng `React.createElement()`.
- Tạo `wrapper` là `React.Fragment` chứa 3 phần:
  1. **Button**
     - Text: `"Nhấn tôi"`
     - Có style object `{ backgroundColor: '#007bff', color: 'white', border: 'none', borderRadius: '4px' }`
     - Khi nhấn: hiển thị alert `"Bạn đã nhấn button!"`
  2. **Card**
     ```html
     <div class="card">
       <h2>Thông tin</h2>
       <p>Đây là một card đơn giản</p>
     </div>
     ```
  3. **Danh sách sản phẩm**
     - Dữ liệu từ mảng:
       ```js
       const products = [
         { name: "Sản phẩm 1", price: 100000 },
         { name: "Sản phẩm 2", price: 200000 },
         { name: "Sản phẩm 3", price: 150000 },
       ];
       ```
     - Render bằng `.map()` thành các `<li>` có prop `key`.

---

## 2️⃣ jsx.html — JSX & Component Practice

### 🎯 Mục tiêu

Hiểu cách **viết JSX trực tiếp trong HTML** và tạo **component với props**.

### 🧩 Nội dung

- Dùng **React**, **ReactDOM**, **Babel** CDN để cho phép JSX.
- Tạo component `Button` với props:
  - `primary` → thêm lớp `.btn-primary`
  - `rounded` → thêm lớp `.btn-rounded`
  - `bordered` → thêm lớp `.btn-bordered`
  - `href` → nếu có, render `<a>` thay vì `<button>`
  - `size` → `"s" | "m" | "l"` (mặc định `"m"`)
- Các props khác (vd: `type`, `target`, ...) được truyền thẳng vào phần tử.
- CSS cơ bản:
  - Base: nền xám nhạt, border none, transition 0.2s
  - Hover: opacity 0.8
  - `.btn-primary`: nền xanh đậm, hover xanh sáng hơn
  - `.btn-bordered`: viền 2px, nền transparent, hover nền xanh nhạt

### 🧱 Render 5 button ví dụ

1. Normal button — `type="button"`
2. Primary button — `type="submit"` + `primary` + `rounded` + `bordered`
3. Rounded button — chỉ `rounded`
4. Bordered button — chỉ `bordered`
5. Link button — `href="https://google.com"` + `target="_blank"` + `primary`

---

## 3️⃣ jsx-map.html — Render List with map()

### 🎯 Mục tiêu

Thực hành **render danh sách** trong React bằng `.map()`.

### 🧩 Nội dung

- Tạo mảng:
  ```js
  const tasks = [
    { id: 1, title: 'Học React cơ bản', isCompleted: true },
    { id: 2, title: 'Tìm hiểu JSX', isCompleted: false },
    ...
  ];
  ```
- Render `<ul>` chứa các `<li>` hiển thị `title`.
- Khi `isCompleted === true`, áp dụng style:
  ```css
  text-decoration: line-through;
  ```

---

## ⚙️ Yêu cầu chung

- Dùng **React**, **ReactDOM**, **Babel** CDN.
- Viết **CSS internal** trong từng file HTML.
- Không sử dụng build tools (Vite, CRA...).

---

## 🧾 Gợi ý chạy

Mở trực tiếp file `index.html` trong trình duyệt.
