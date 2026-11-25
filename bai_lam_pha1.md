# BÀI LÀM PHA 1 

- **Họ tên:**
- **Lớp:**
- **Link repository Pha1:**

> Pha 1 (70 phút đầu, KHÔNG dùng AI). Viết xong, kéo thả file này vào repository Pha1 trước mốc giờ giám thị công bố.

## 4.1. Bảo vệ dữ liệu và chống ảo giác

### a) Ghi chú đã ẩn danh hoá

**GHI CHU DA AN DANH**

```text
(Viết đoạn ghi chú đã ẩn danh hoá vào đây – xoá dòng này)
```

### b) Hai câu lệnh chống ảo giác

**CAU LENH**

```text
(Viết câu 1 và câu 2 vào đây – xoá dòng này)
```

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**PROMPT**

```text
C-CONTEXT
Bạn là nhân viên mới của Ban tổ chức giải bóng đá Cúp Sao Vàng, phụ trách hỗ trợ khán giả mua vé các trận đấu. Trưởng ban giao cho bạn xây dựng bộ prompt để xử lý thông tin khán giả, tin nhắn đặt vé, báo giá và khiếu nại một cách an toàn, chính xác.
R-REQUEST
xử lý thông tin khán giả, tin nhắn đặt vé, báo giá và khiếu nại một cách an toàn, chính xác.
E_EXPLANATION
không lấy thông tin giã phải đảm bảo tính xác thật và nhất quán với tin nhắn 
không tự ý sữa đổi các thông tin 
không lấy thông tin khách hàng 
đơn giá không lấy âm 
số lượng phải hơn 1 mới lên đơn 
chỉ trả về JSON
A-ACTION
1. Nhận tin nhắn và trích dẫn thông tin khách hàng 
2. KIểm tra tính hợp lệ của dữ liệu 
3. xác nhận số lượng và lịch sữ đặt vé
T-TONE
không chào hỏi, không giải thích
viết dưới ngôn ngữ trang trọng
E-EXTRAS
<doi_tuong_1>
<doi_tuong_2>
<doi_tuong_3>

```

## 4.3. Báo giá vé bằng Chain-of-Thought

### a) Prompt

**PROMPT**
C - Context
Bạn là nhân viên mới của Ban tổ chức giải bóng đá Cúp Sao Vàng, phụ trách hỗ trợ khán giả mua vé các trận đấu.
R - Request
Thu thập và phân tích dữ liệu 
E - Explanation
không tự láy thông tin cá nhân khách hàng 
chỉ lấy thông tin cần cho việt báo cáo tài chính được cung cấp từ tin nhắn 
chỉ trả về JSON, không chào hỏi, không giải thích.
A - Action
1. Nhận tin nhắn và trích dẫn thông tin khách hàng 
2. KIểm tra tính hợp lệ của dữ liệu 
3. Phân loại vé thường , vip , null
4. Lên đon tính giá tiền 
T - Tone
ngôn ngứ dễ đọc dễ hiểu 
có thể tích hợp tiếng anh
định dạng rõ ràng phù hợp
E - Extras.
few-shot 
đầu vào  : tôi mua 2 vé thường và 3 vé vip 
đầu ra  : 
so luong : 5
vip : 3 x 200.000
thuong : 2 x 100.000
tong : 800.000
```text
)
```

## 4.4. Dây chuyền xử lý khiếu nại (Prompt Chaining)

### a) Prompt Trạm 1

**PROMPT**

```text
(Viết prompt vào đây – xoá dòng này)
```

### b) Hai điều cần kiểm tra ở JSON đầu ra của Trạm 1

1. (Viết câu trả lời vào đây – xoá dòng này)

2.

### c) Câu lệnh viết tiếp

**CAU LENH**

```text
(Viết câu lệnh vào đây – xoá dòng này)
```

## 4.5. Prompt chấm bài theo Rubric

**PROMPT**

```text
(Viết prompt vào đây – xoá dòng này)
```

## 4.6. Hoàn thiện System Prompt

> Phần Vai trò và Chuẩn đầu ra đã cho sẵn. Viết tiếp phần Quy tắc ràng buộc và Xử lý ngoại lệ.

```text
[Vai trò]
Bạn là "Trợ lý Cúp Sao Vàng", nhân viên tư vấn vé và dịch vụ trên website của giải bóng đá Cúp Sao Vàng, giúp khán giả chọn và đặt một trong 3 gói: SVT (Sân Vận Động – vé trận đấu), FZ (Fan Zone – khu cổ vũ), VIP (Khán đài VIP).

[Quy tắc ràng buộc]
1. (Viết quy tắc 1 – xoá dòng này)
2.
3.

[Chuẩn đầu ra]
Trả lời bằng tiếng Việt, lịch sự, tối đa 120 từ. Giá vé trình bày dạng gạch đầu dòng. Kết thúc bằng một câu hỏi về nhu cầu tiếp theo của khách.

[Xử lý ngoại lệ]
- Khách hỏi ngoài phạm vi: (Viết cách trả lời – xoá dòng này)
- Khách cung cấp thiếu thông tin:
```
