# Admin Oriagent

*Automatically synced with your [v0.app](https://v0.app) deployments*

[![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?style=for-the-badge&logo=vercel)](https://vercel.com/hexcodeai/admin-oriagent)
[![Built with v0](https://img.shields.io/badge/Built%20with-v0.app-black?style=for-the-badge)](https://v0.app/chat/projects/3TFF5m8Cx9d)

## Overview

This repository will stay in sync with your deployed chats on [v0.app](https://v0.app).
Any changes you make to your deployed app will be automatically pushed to this repository from [v0.app](https://v0.app).

## Deployment

Your project is live at:

**[https://vercel.com/hexcodeai/admin-oriagent](https://vercel.com/hexcodeai/admin-oriagent)**

## Build your app

Continue building your app on:

**[https://v0.app/chat/projects/3TFF5m8Cx9d](https://v0.app/chat/projects/3TFF5m8Cx9d)**

## How It Works

1. Create and modify your project using [v0.app](https://v0.app)
2. Deploy your chats from the v0 interface
3. Changes are automatically pushed to this repository
4. Vercel deploys the latest version from this repository

1. npm install next react react-dom

2. npm install
3. npm run dev

1. npx prisma migrate dev
npm run prisma-seed   
 npm i --legacy-peer-deps
 

 Ok 👍 mình sẽ giải thích chi tiết từng lệnh nhé:

---

### 1. **`npx prisma migrate dev`**

* **Mục đích:** Dùng để **chạy migration** trong môi trường phát triển khi dùng **Prisma ORM**.
* Hoạt động:

  1. Prisma đọc file `schema.prisma` (nơi bạn định nghĩa **model database**).
  2. Sinh ra migration SQL trong thư mục `prisma/migrations/`.
  3. Thực thi migration đó vào database (tạo bảng, chỉnh sửa cột, quan hệ, v.v).
  4. Cập nhật file `prisma/client` để đồng bộ code với schema.
* Tương đương: `"tạo/cập nhật cấu trúc database theo schema.prisma"`.

---

### 2. **`npm run prisma-seed`**

* **Mục đích:** Chạy script **seed database** (tạo dữ liệu mẫu ban đầu).
* Thường trong `package.json` có cấu hình:

  ```json
  "scripts": {
    "prisma-seed": "ts-node prisma/seed.ts"
  }
  ```
* Khi chạy, nó sẽ insert một số dữ liệu mặc định vào database, ví dụ:

  * User admin mặc định.
  * Một số sản phẩm demo.
  * Dữ liệu test.

👉 Giúp bạn không phải nhập tay từng record khi mới setup dự án.

---

### 3. **`npm i --legacy-peer-deps`**

* **Mục đích:** Cài đặt dependency nhưng **bỏ qua lỗi peerDependencies**.
* Từ npm v7 trở lên, khi cài các package có **peerDependencies** không khớp (ví dụ package A yêu cầu React 17 nhưng bạn đang dùng React 18), npm sẽ báo lỗi.
* Flag `--legacy-peer-deps` cho npm cài **theo kiểu cũ** (npm v6), tức là bỏ qua check đó.

👉 Dùng khi:

* Bạn gặp lỗi kiểu:

  ```
  ERESOLVE could not resolve
  ```
* Hoặc dependency của bạn chưa update để support version mới.

---

✅ Tóm lại:

* `npx prisma migrate dev` → Đồng bộ schema Prisma với database.
* `npm run prisma-seed` → Nạp dữ liệu mẫu vào database.
* `npm i --legacy-peer-deps` → Cài đặt dependencies mà bỏ qua check peer deps (tránh lỗi version).

---

Bạn có muốn mình viết luôn **flow chuẩn khi setup dự án Prisma + Next.js** (bao gồm migrate, seed, run dev) để bạn copy chạy không?

 # admin-aihive-app
