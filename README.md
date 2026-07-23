# Thám Tử Nhí

Game rèn luyện khả năng quan sát và trí nhớ cho học sinh tiểu học.

## Chơi thử ngay

Mở file `play-now.html` bằng trình duyệt. Bản này chạy độc lập, không cần cài package.

Trang riêng cho bé 5 tuổi học số và chữ cái: `little-abc-123.html`.

Khi deploy GitHub Pages, URL gốc sẽ tự mở `little-abc-123.html`.

## Deploy GitHub Pages

GitHub Pages dùng nhánh `main`, thư mục gốc `/`. Sau khi push lên GitHub và bật Pages, site sẽ public cho bé chơi ở nhà.

Các file cần public:

- `index.html`
- `little-abc-123.html`
- `play-now.html`
- `tts/`

## Chạy theo stack Angular + NestJS

Khi máy truy cập được npm registry:

```bash
npm install
npm run dev
```

- Angular frontend: `http://localhost:4200`
- NestJS API: `http://localhost:3000/api/game/adventure`

## Gameplay hiện có

- Core loop theo RSD: nhận nhiệm vụ, vào world, giải puzzle, nhận thưởng, mở khóa vault.
- Quan sát lớp học rồi trả lời câu hỏi chi tiết.
- Ghi nhớ vị trí đồ vật trên bảng 3x3.
- Nhớ và bấm lại đúng chuỗi biểu tượng.
- Tìm món đồ vừa biến mất khỏi bảng quan sát.
- Đếm nhanh số đồ vật cùng màu.
- Ghi nhớ đường đi bí mật trên bảng 9 ô.
- Logic Puzzle: number pattern, odd one out, relationship, conditional logic.
- Pattern Puzzle, Math Puzzle, Maze Puzzle, Robot Programming Puzzle, Deduction Puzzle.
- Toán vượt chướng ngại vật: trả lời nhiều phép tính để vượt vật cản và nhận điểm.
- Xếp hình kho báu: di chuyển mảnh cạnh ô trống để hoàn thành bản đồ.
- Tìm hình giống nhau: lật thẻ và ghép đủ các cặp hình.
- Chế độ chơi theo nhóm: luân phiên Đội Tia Chớp / Đội Sao Nhỏ và cộng Knowledge Points cho đội.
- Nút chọn world và chế độ chơi ở màn đầu đã có xử lý tương tác thật.
- Reward: score, star, XP, coins, Knowledge Points.
- Achievement, Daily Mystery message, Team Quest progress, Knowledge Vault unlock preview.
- Mỗi lượt bắt đầu sẽ random cảnh chơi, thứ tự màn, câu hỏi, đáp án, mục tiêu và chuỗi ký ức.
- Tính điểm, sao, phản hồi đúng/sai và lưu kết quả tạm.
- Vườn ABC 123: tab riêng cho bé 5 tuổi học số, chữ cái, đếm đồ vật, tìm cặp chữ-hình và tập tô chữ.
- Cơ chế học để chơi: mỗi câu/cặp/nhiệm vụ đúng cộng 1 điểm, đủ 10 điểm mở game thưởng "Bắn chim giấy nhận sao".

## API scaffold theo RSD

- `GET /api/game/adventure`: random adventure/puzzle session.
- `GET /api/game/catalog`: worlds, characters, puzzle types, reward rules, team quest, knowledge vault.
- `POST /api/game/attempts`: lưu kết quả tạm.
