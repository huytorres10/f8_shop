1. Dụng source base
base.css: config chung css cho dự án.
main.css: Code riêng css cho dự án, sau này mỗi component sẽ chứa các file css khác nhau

2. Reset CSS
key search: normalizer css cdn
web: https://cdnjs.com/libraries/normalize
- Dùng cdn = link <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css" />
- Hoặc tải file xuống rồi nhét vào thư mục assets/css

3. Dựng base CSS
box-sizing: inherit; : Kế thừa thằng cha có box-sizing
key search: google roboto font
web: https://fonts.google.com/specimen/Roboto
- Select type font mong muốn
+ Copy link dán vào file html
+ Copy font-family: 'Roboto', sans-serif; vào file CSS
.grid {
	width: 1200px;
	max-width: 100%;
}
- Đối với màn hình từ 1200px trở lên thì khung web sẽ hiển thị là 1200px.
- Đối với màn hình nhỏ hơn 1200px thì nó sẽ luôn hiện 100% thao giao diện trình duyệt.
