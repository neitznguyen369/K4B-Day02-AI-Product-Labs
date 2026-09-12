# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Nguyễn Mạnh Tiến
- Mã học viên: 2A202602506
- Vai trò / bối cảnh (VD: sinh viên năm 4, intern PM, ...):
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
  - Đi học
  - Đi chợ 
  - Đi cafe
  - Làm việc

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

## Bảng scan

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật / giả định cần kiểm chứng |
|---|---|---|---|---|
| 1 | Lặp lại | Mua rau, trứng, thịt nhưng không ghi lại hoặc cập nhật inventory | Sinh viên, người sống một mình | Sau khi đi chợ thường nhớ không đầy đủ; cần hỏi 5-7 người |
| 2 | Tốn thời gian | Mở tủ lạnh rồi mất nhiều phút nghĩ hôm nay nấu gì | Người bận rộn, sinh viên | Có xu hướng chuyển sang đặt đồ ăn; cần đo số lần/tuần |
| 3 | AI có thể tốt hơn | Không biết nguyên liệu nào nên dùng trước khi nhiều món cùng sắp hết hạn | Người mua thực phẩm theo tuần | Có nhiều ngày cần dùng gần nhau; cần thử nhật ký inventory |
| 4 | Pain từ người khác | Mua trùng hành, trứng, sữa vì không nhớ ở nhà còn gì | Người ở trọ, hộ nhỏ | Hóa đơn mua trùng và lời phàn nàn “ở nhà còn mà quên” |
| 5 | Tốn thời gian | Có nguyên liệu nhưng không ghép được thành món đủ đơn giản | Người không tự tin nấu ăn | Phải tìm công thức nhiều nguồn, khoảng 10-20 phút/lần |
| 6 | Lặp lại | Cuối tuần kiểm tra thực phẩm nào đã hỏng và phải bỏ đi | Người mua thực phẩm tươi | Xảy ra khoảng mỗi tuần; cần ghi lượng/giá trị bỏ đi |
| 7 | Pain từ người khác | Kế hoạch ăn không hợp với lịch học/lịch làm thay đổi | Sinh viên, người đi làm | Đã mua nhưng bận nên không dùng đúng kế hoạch |
| 8 | AI có thể tốt hơn | Nhắc hạn sử dụng nhưng không gắn với món ăn hoặc hành động cụ thể | Người dùng app nhắc việc | Reminder chung dễ bị bỏ qua; cần test hành động sau nhắc |
| 9 | Tốn thời gian | Đọc nhiều công thức để tìm món vừa dùng được nguyên liệu vừa hợp khẩu vị | Người có ít nguyên liệu | Phải lọc thủ công nhiều điều kiện |
| 10 | Lặp lại | Sau khi nấu không cập nhật phần nguyên liệu còn lại | Người ở một mình | Inventory nhanh sai sau mỗi bữa; cần thử cập nhật dưới 30 giây |

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Không biến inventory trong tủ lạnh thành kế hoạch dùng thực phẩm trước hạn | Actor rõ, xảy ra hằng tuần, tác động đến tiền và lãng phí, có metric | Người dùng có chịu nhập inventory và hạn dùng không? |
| 2 | Mua trùng nguyên liệu vì không nhớ trong tủ còn gì | Pain rõ, có thể giải bằng inventory đơn giản | Có đủ thường xuyên để cần workflow riêng không? |
| 3 | Có nguyên liệu nhưng không nghĩ ra món phù hợp với thời gian và khẩu vị | AI có thể tổng hợp nhiều điều kiện | Có thể lệch thành bài toán “tìm công thức” |


### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

# Problem Card #1 — Cứu Tủ Lạnh

**Problem :** Sinh viên hoặc người sống một mình thường không biến được inventory và hạn sử dụng trong tủ lạnh thành kế hoạch ăn, nên chỉ phát hiện thực phẩm sắp hỏng khi đã quá muộn.

**Actor:** Sinh viên hoặc người sống một mình, tự mua thực phẩm và tự quyết định bữa ăn.

**Thời điểm / bối cảnh:** Sau khi đi chợ và mỗi tối trước khi quyết định ăn gì; đặc biệt vào cuối tuần khi kiểm tra lại tủ lạnh.

**Current workflow:**
1. Mua thực phẩm theo cảm tính hoặc theo danh sách cũ.
2. Cất vào tủ lạnh nhưng không ghi đầy đủ số lượng và hạn dùng.
3. Đến giờ ăn thì mở tủ, nhìn nhanh và cố nhớ mình còn gì.
4. Tìm công thức hoặc đặt đồ ăn nếu không nghĩ ra món.
5. Cuối tuần phát hiện một phần thực phẩm đã hỏng và bỏ đi.

**Bottleneck:** Bước 3-4: biến danh sách nguyên liệu không đầy đủ thành thứ tự ưu tiên và món ăn phù hợp. Baseline giả định: 10-15 phút/lần quyết định bữa tối, 3-5 lần/tuần.

**Impact:** Lãng phí thực phẩm, mua trùng, tốn tiền và tăng khả năng đặt đồ ăn dù trong tủ vẫn còn nguyên liệu.

**Success metric:** Trong pilot 2 tuần, giảm thời gian quyết định bữa tối từ 10-15 phút xuống dưới 5 phút; ít nhất 70% nguyên liệu được đánh dấu “cần dùng” được dùng hoặc xử lý trước ngày user nhập; không tăng số lần bỏ món vì gợi ý không phù hợp.

**Non-AI alternative:** Bảng inventory có tên, số lượng, ngày mua, ngày cần dùng và màu cảnh báo; kế hoạch ăn cố định 3-4 món/tuần. Cách này giải quyết việc nhớ hạn nhưng chưa tốt ở việc ghép nhiều nguyên liệu theo context.

**AI hypothesis:** Khi người dùng cung cấp inventory, ngày cần dùng, khẩu vị và thời gian nấu, AI có thể đề xuất thứ tự ưu tiên cùng 2-3 món đơn giản. AI chỉ draft; người dùng xác nhận inventory và chọn món.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[X] Workflow
[ ] Agent
[ ] Chưa biết

## Draft workflow card #1

```text
CURRENT STATE — khoảng 10-15 phút/lần quyết định bữa ăn

[Mua và cất thực phẩm]
        -> [Nhớ/đoán inventory]
        -> [Mở tủ và kiểm tra nhanh]
        -> [Tìm công thức hoặc nghĩ món: 10']  <-- bottleneck
        -> [Không chắc thì đặt đồ ăn]
        -> [Cuối tuần bỏ đồ đã hỏng]

FUTURE STATE — mục tiêu dưới 5 phút/lần

[User nhập/chụp inventory + ngày cần dùng]
        -> [Rule sắp xếp theo ngày cần dùng]
        -> [AI draft 2-3 món theo inventory, thời gian, khẩu vị]
        -> [User kiểm tra inventory và chọn món: 2-3'] <-- human boundary
        -> [Nấu và bấm cập nhật phần còn lại]

Fallback: AI draft tệ hoặc dữ liệu thiếu -> user dùng bảng inventory
và bộ công thức cố định.
```
# Problem Card #2 — Chống mua trùng

**Problem :** Người sống một mình thường mua lại nguyên liệu đang có vì inventory không được cập nhật và khó kiểm tra trước khi đi chợ.

**Actor:** Người đi chợ 1-2 lần/tuần, có tủ lạnh nhỏ.

**Bối cảnh:** Trước khi đi mua đồ.

**Current workflow:** Nhớ trong đầu -> xem nhanh tủ lạnh -> viết danh sách -> mua thêm -> phát hiện đồ trùng.

**Bottleneck:** Kiểm tra inventory nhanh nhưng đủ chính xác trước khi mua.

**Impact:** Tốn tiền, tủ chật, tăng nguy cơ thực phẩm không được dùng.

**Success metric:** Giảm số lần mua trùng trong 2 tuần; thời gian kiểm tra danh sách dưới 3 phút.

**Non-AI alternative:** Checklist inventory tối giản, cập nhật bằng checkbox sau mỗi lần mua hoặc dùng.

**AI hypothesis:** AI đối chiếu danh sách mua với inventory và hỏi lại các mục có khả năng trùng.

Quick gut:
[X] No AI / process fix
[ ] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — khoảng 5-10 phút trước mỗi lần đi mua đồ

[Nhớ trong đầu còn gì]
        → [Mở tủ và kiểm tra nhanh]
        → [Viết danh sách mua]
        → [Mua thêm nguyên liệu]
        → [Về nhà phát hiện đồ trùng]  <-- bottleneck

FUTURE STATE — mục tiêu dưới 3 phút

[Mở checklist inventory đã cập nhật]
        → [Đánh dấu số lượng còn lại]
        → [So sánh với danh sách mua]
        → [User xác nhận mục nào thật sự cần mua]  <-- human boundary
        → [Mua và cập nhật checklist]

Fallback: checklist chưa cập nhật hoặc không chắc số lượng -> kiểm tra trực tiếp
tủ lạnh trước khi mua; không tự động loại sản phẩm khỏi danh sách.
```

---

# Problem Card #3 — Ghép món từ nguyên liệu sẵn có

**Problem 1 câu:** Người dùng có nguyên liệu trong tủ nhưng mất nhiều thời gian tìm món phù hợp với số lượng, khẩu vị và thời gian nấu.

**Actor:** Người mới nấu hoặc người bận rộn.

**Bối cảnh:** Trước mỗi bữa ăn.

**Current workflow:** Nhìn nguyên liệu -> tìm công thức -> mở nhiều công thức -> kiểm tra nguyên liệu thiếu -> bỏ cuộc hoặc đặt đồ ăn.

**Bottleneck:** Lọc và tổng hợp công thức theo inventory thật, không phải theo nguyên liệu lý tưởng.

**Impact:** Tốn thời gian, bỏ phí nguyên liệu và giảm số bữa tự nấu.

**Success metric:** Từ 15-20 phút tìm món xuống dưới 5 phút; món được chọn dùng ít nhất 70% nguyên liệu có sẵn.

**Non-AI alternative:** Bộ công thức cố định được tag theo nguyên liệu, thời gian và độ khó.

**AI hypothesis:** AI tổng hợp nhiều ràng buộc để đề xuất món thay thế khi thiếu nguyên liệu.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[X] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — khoảng 15-20 phút/lần tìm món

[Nhìn nguyên liệu đang có]
        → [Tìm công thức trên nhiều nguồn]
        → [Mở và so sánh nhiều công thức]
        → [Kiểm tra nguyên liệu thiếu, thời gian và khẩu vị]  <-- bottleneck
        → [Bỏ cuộc hoặc đặt đồ ăn]

FUTURE STATE — mục tiêu dưới 5 phút

[User nhập inventory, khẩu vị và thời gian nấu]
        → [AI lọc và draft 2-3 món phù hợp]
        → [AI nêu nguyên liệu thiếu và phương án thay thế]
        → [User kiểm tra tính khả thi và chọn món]  <-- human boundary
        → [Nấu món đã chọn]

Fallback: AI gợi ý món không phù hợp hoặc thiếu nguyên liệu quan trọng ->
user bỏ draft, dùng bộ công thức cố định đã tag theo nguyên liệu và thời gian.
```
---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card:** Problem Card #1 — biến inventory thành kế hoạch dùng thực phẩm trước hạn.

**Vì sao:** Đây là điểm nối giữa các pain nhỏ: quên inventory, không biết nấu gì, mua trùng và bỏ đồ hỏng. Workflow có thể giới hạn trong một bước, có baseline thời gian và boundary rõ.

**Câu hỏi muốn nhóm challenge:** Người dùng có thực sự chịu nhập inventory và hạn dùng đủ đều không? Nếu không, cần hỗ trợ nhập nhanh ở mức nào trước khi thêm AI?

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra:
- Tôi sửa gì:

### Self-check nộp phần 01
- [X] Có 5+ problems + top 3 Cards đủ field
- [X] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [X] Đã chọn 1 card pitch + câu hỏi challenge
