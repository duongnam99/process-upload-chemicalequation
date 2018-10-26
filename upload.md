# Upload process
- setup Elastic trên server
- migrate để tạo cột slug, seo title, description cho bảng chemical_equation và cột slug cho bảng equation_tag
- chạy command: 
    - Khởi tạo dữ liệu cho elastic: `php artisan init:elastic --data chemical --action create` và `php artisan init:elastic --data equation --action create`
    - Gen slug cho phương trình và cate: `php artisan slug:gen --type equation`, `php artisan slug:gen --type cate`
    - Gen seo title cho phương trình hóa học: `php artisan seo:equation`
- **Lưu ý các hàm setup elastic trong model**