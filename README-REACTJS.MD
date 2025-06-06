# Note React
## Tạo dự án: 
```
npx create-react-app .
```
- Build lại react mỗi lần cài thự viện
```
docker-compose build react
docker-compose up -d react
```

## Các gói cần cài đặt
- Tailwindcss:
```
npm install -D tailwindcss@3 postcss autoprefixer
npx tailwindcss init -p
```
- Cài đặt các route cho trang web
```
npm install react-router-dom
```

## Trường hợp lỗi
- Lỗi: 157 vulnerabilities (xxx moderate, xx high, xx critical)
- Xử lý: Khi cài đặt npm chạy thêm:
```
npm set audit false
```
- hoặc chạy: 
```
npm audit fix --force
```
- Lỗi: Error: error:0308010C:digital envelope routines::unsupported (từ node 18 trở lên)
- Xử lý: vào package.json cập nhật lại các "scripts" khi khởi động
```
"scripts": {
    "start": "react-scripts --openssl-legacy-provider start",
    "dev": "react-scripts --openssl-legacy-provider start",
    "build": "react-scripts --openssl-legacy-provider build",
    "test": "react-scripts --openssl-legacy-provider test",
    "eject": "react-scripts --openssl-legacy-provider eject"
  },
```

## Practice React
- Được note lại trong: ./src