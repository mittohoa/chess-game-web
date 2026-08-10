# chess-game-web

Trang giới thiệu cho app **Cờ Vua**, phục vụ qua GitHub Pages tại
**https://mittohoa.github.io/chess-game-web/**

Repo này **chỉ chứa trang web**. Mã nguồn app nằm ở repo riêng và không công khai.

## Vì sao tách khỏi repo mã nguồn

GitHub Pages phục vụ mọi tệp trong repo cho bất kỳ ai. Để trang giới thiệu công
khai mà mã nguồn vẫn riêng tư, hai thứ phải nằm ở hai repo khác nhau.

## Cấu trúc

```
index.html      # toàn bộ trang, không phụ thuộc thư viện ngoài
anh/            # ảnh chụp màn hình
```

Trang tự chứa hoàn toàn: không CDN, không phông tải về, không script theo dõi.
Mở thẳng `index.html` bằng trình duyệt là xem được.

## Ảnh từ đâu ra

Ảnh trong `anh/` **được dựng từ chính mã nguồn app**, không phải chụp tay, nên
không bao giờ lệch khỏi giao diện thật. Ở repo mã nguồn chạy:

```bash
flutter test tool/design_preview_test.dart --update-goldens
```

rồi chép sang đây:

| Tệp nguồn (repo mã nguồn) | Tệp đích |
| --- | --- |
| `docs/web/anh-app.png` | `anh/anh-app.png` |
| `docs/thiet-ke/bo-quan.png` | `anh/bo-quan.png` |
| `docs/thiet-ke/bo-quan-tren-ban.png` | `anh/bo-quan-tren-ban.png` |

## Cập nhật trang

Sửa `index.html`, xem thử bằng trình duyệt, rồi đẩy lên `main`. GitHub Pages tự
dựng lại sau khoảng một phút.

## Liên hệ

mittohoa@gmail.com
