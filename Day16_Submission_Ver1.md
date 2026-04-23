# Day 16 Submission — Team [tên team]

## Student
- A202600404 - Nguyễn Thành Đại Khánh

---

## 1. Idea Reframed

Original idea:
> Xây dựng công cụ AI giúp sinh viên và fresher review CV và luyện phỏng vấn trước khi ứng tuyển việc làm.

Reframed as a product opportunity:
> Sinh viên năm cuối và fresher tại Việt Nam đang bước vào thị trường lao động cạnh tranh mà không có phản hồi cá nhân hóa — họ không biết CV của mình yếu ở đâu, và không có môi trường an toàn để luyện phỏng vấn thật sự. Các công cụ hiện tại (template CV, blog tips, CLB mock interview) không đủ thông minh, không cá nhân hóa, và không có mặt đúng lúc người dùng cần nhất. Cơ hội ở đây là xây một công cụ AI chạy gap analysis CV–JD và mô phỏng phỏng vấn theo ngành VN — available 24/7, không cần đặt lịch với ai.

---

## 2. Customer / Segment Card

- **Segment name:** Sinh viên năm 3–4 khối ngành Kinh tế / Công nghệ tại các trường Đại học trọng điểm (Hà Nội & TP.HCM), đang có kế hoạch ứng tuyển Internship hoặc Full-time lần đầu trong 6 tháng tới.

- **Operational context:** Người dùng đang trong giai đoạn chuẩn bị ứng tuyển (viết CV, nộp hồ sơ, chuẩn bị phỏng vấn). Thường truy cập các nền tảng tìm việc (LinkedIn, TopCV, VietnamWorks). Thiếu kinh nghiệm thực tế về cách viết CV chuẩn và trả lời phỏng vấn. Thường tự tìm hiểu qua Google, YouTube nhưng thông tin rời rạc, không cá nhân hóa.

- **Recurring workflow:**
  1. Tìm mẫu CV trên mạng
  2. Viết CV theo cảm tính hoặc copy mẫu
  3. Nộp CV cho nhiều công ty
  4. Nhận ít phản hồi hoặc bị từ chối
  5. Chuẩn bị phỏng vấn một cách mơ hồ
  6. Lặp lại quá trình khi apply job mới

- **Pain moment:** Sau khi nộp CV nhưng không nhận được phản hồi. Khi được gọi phỏng vấn nhưng không biết trả lời như thế nào. Không biết CV của mình đang sai ở đâu. Mất tự tin vì bị từ chối nhiều lần.

- **Why now:** Thị trường lao động cạnh tranh cao, sinh viên cần chuẩn bị tốt hơn. LLM hiện tại đã đủ mạnh để phân tích CV, gợi ý chỉnh sửa cá nhân hóa, và giả lập phỏng vấn. Gen Z quen dùng AI — dễ tiếp cận sản phẩm. Các công cụ hiện tại (CV templates) chưa thông minh và chưa cá nhân hóa sâu.

- **Access path:** Tích hợp trên website tạo CV (TopCV, Canva) và nền tảng học tập / trường đại học. Marketing qua TikTok, Facebook (nội dung hướng nghiệp) và cộng đồng sinh viên. Freemium model: Free = review CV cơ bản; Paid = mock interview + feedback sâu.

One-sentence description:
> Sinh viên năm cuối ngành Kinh tế / Công nghệ tại HN & HCM đang chuẩn bị apply lần đầu — họ có deadline rõ ràng, có pain thật, nhưng không có công cụ nào đủ thông minh để giúp họ biết mình đang sai ở đâu.

---

## 3. Need Map

### Need #1 (priority) — Không biết CV của mình yếu ở đâu và tại sao bị loại

- **Statement (JTBD):** Khi tôi nộp CV mà không nhận được phản hồi, tôi muốn biết chính xác CV của mình đang thiếu gì và bị loại ở điểm nào, để tôi có thể sửa đúng chỗ thay vì đoán mò.
- **Current workaround:** Nhờ bạn bè hoặc anh chị xem qua; tham khảo CV mẫu trên TopCV, VietnamWorks rồi tự so sánh.
- **Pain signal:** Nộp 10–20 chỗ không ai gọi lại; không nhận được bất kỳ feedback nào từ nhà tuyển dụng; không biết sửa gì để lần sau khác đi.
- **Evidence / proxy evidence:** Các hệ thống ATS lọc CV theo keyword — nhiều CV bị loại tự động trước khi có người đọc. Trên các group Facebook sinh viên, dạng bài "nhờ mọi người xem CV giúp mình" xuất hiện thường xuyên, cho thấy nhu cầu có phản hồi nhưng thiếu kênh chính thức. *(Cần user interview để xác nhận định lượng.)*
- **Why underserved:** Nhà tuyển dụng không có thời gian feedback từng CV bị loại. Bạn bè / mentor không đủ chuyên môn để đánh giá theo tiêu chuẩn ngành. Không có công cụ nào tự động so khớp CV với JD và giải thích lý do gap.

### Need #2 — Không có môi trường an toàn để luyện phỏng vấn thật sự

- **Statement (JTBD):** Khi tôi được gọi phỏng vấn nhưng chưa bao giờ phỏng vấn thật, tôi muốn được luyện tập với câu hỏi sát thực tế và nhận phản hồi ngay sau mỗi câu trả lời, để tôi không bị bất ngờ và tự tin hơn khi vào phòng phỏng vấn thật.
- **Current workaround:** Tự luyện một mình trước gương hoặc đọc câu hỏi phổ biến trên mạng; tham gia mock interview của CLB (nếu có).
- **Pain signal:** Vào phỏng vấn thật bị hỏi những câu không chuẩn bị; trả lời lan man, thiếu cấu trúc; mất tự tin sau khi bị từ chối.
- **Evidence / proxy evidence:** Các video tips phỏng vấn trên YouTube VN của Glints, TopCV đạt hàng trăm nghìn lượt xem — signal về nhu cầu chuẩn bị lớn. Mock interview CLB thường kín slot và lịch cứng — supply không đủ đáp ứng demand. *(Cần phỏng vấn 5–10 fresher để xác nhận willingness to pay.)*
- **Why underserved:** CLB mock interview có slot giới hạn, lịch cứng, không available đúng lúc người dùng cần. Dịch vụ freelance coach phỏng vấn chậm và đắt. Không có công cụ nào sinh câu hỏi từ chính JD người dùng đang apply và cho phản hồi theo rubric cụ thể.

### Need #3 (optional) — Nhận feedback cụ thể, có thể hành động ngay

- **Statement (JTBD):** Khi tôi nhận được góp ý về CV hoặc phỏng vấn, tôi muốn biết chính xác cần sửa gì, sửa như thế nào, và ưu tiên sửa cái nào trước, để tôi không lãng phí thời gian cải thiện sai chỗ.
- **Current workaround:** Nhờ bạn bè hoặc mentor góp ý không thường xuyên; đọc blog tips chung chung.
- **Pain signal:** Nhận được góp ý kiểu "CV nhìn ổn nhưng cần cải thiện" — không biết cải thiện cái gì cụ thể.
- **Evidence / proxy evidence:** Trên các diễn đàn sinh viên, câu hỏi dạng "CV của mình đã ổn chưa ạ?" xuất hiện thường xuyên — signal rằng feedback hiện tại không đủ rõ để người dùng tự đánh giá.
- **Why underserved:** Feedback từ bạn bè thiếu tiêu chuẩn và không nhất quán. Nhà tuyển dụng không feedback. Không có hệ thống đánh giá theo rubric chuẩn ngành với output cụ thể.

---

## 4. Strategy Statement

For sinh viên năm cuối & fresher (0–1 năm kinh nghiệm) đang tìm việc lần đầu tại Việt Nam,

who struggle with không biết CV của mình yếu ở đâu và không có môi trường an toàn để luyện phỏng vấn thật sự,

our product helps them tự tin bước vào phỏng vấn đầu tiên với CV đã được kiểm tra kỹ và kỹ năng trả lời đã được luyện thật,

through người dùng paste CV + JD vào → hệ thống chạy gap analysis giữa CV thật và yêu cầu JD, highlight đúng 3 điểm yếu ưu tiên nhất → sau đó sinh câu hỏi phỏng vấn từ chính những gap đó → đánh giá câu trả lời theo rubric STAR có điều chỉnh theo ngành VN,

unlike CV mẫu trên TopCV, blog tips chung chung, mock interview CLB (ít slot, lịch cứng), hay dịch vụ freelance coach (chậm, đắt),

because we can leverage LLM đủ mạnh để đọc CV + hiểu JD + sinh câu hỏi phỏng vấn phù hợp ngành, và có thể scale không giới hạn với chi phí gần bằng 0 mỗi session.

---

## 5. Moat Hypothesis

**Moat mechanism:** Distribution lock (ngắn hạn) + Data compounding flywheel (dài hạn)

**Moat giai đoạn đầu (0–12 tháng):** Chiếm kênh phân phối qua partnership với 3–5 trường ĐH lớn và CLB hướng nghiệp tại HN & HCM trước khi đối thủ làm. User có switching cost vì profile, lịch sử CV và session luyện tập đã lưu trong hệ thống.

If we deploy 50 times in the same vertical, the following improve:
1. Độ chính xác của CV feedback theo từng ngành VN (Marketing, IT, Finance...) — càng nhiều CV được review, model càng hiểu chuẩn ngành local và phân biệt được CV tốt/yếu theo từng vị trí cụ thể tại VN.
2. Bộ câu hỏi phỏng vấn theo công ty & vị trí tại VN — tích lũy từ session của user, không có trong LLM gốc, tạo ra dataset độc quyền theo thị trường VN.
3. Benchmark so sánh — "CV của bạn đang ở top bao nhiêu % so với fresher cùng ngành" — chỉ có được khi có đủ data; tạo ra engagement loop mạnh.

Why competitors cannot easily replicate this:
> Data CV & interview pattern của thị trường VN không công khai — đối thủ mới phải tự thu thập từ đầu. Nếu chiếm được kênh phân phối qua trường ĐH & CLB trước, chi phí acquisition của đối thủ sẽ cao hơn đáng kể. Data flywheel là moat mục tiêu tháng 12–18, không phải moat ngày 1.

---

## 6. Initial TAM / SAM / SOM View

| Layer | Estimate | Key Assumptions | Confidence |
|-------|----------|-----------------|------------|
| TAM | $1.5M – $7.5M / year | ~500K SV tốt nghiệp/năm tại VN; 30–40% willing to pay; ARPU ~400K VNĐ/chu kỳ 2 tháng | low |
| SAM | $250K – $420K / year | Chỉ HN + HCM; chỉ ngành Kinh tế + Công nghệ; chỉ năm 3–4 active apply; ~15K–25K paying users/năm | med |
| SOM | $2.5K – $25K / year (năm 1) | 3–5 trường partnership; 150–1.500 paying users; ARPU ~400K VNĐ/chu kỳ | low |

**Top 3 unknowns requiring further research:**
1. **Willingness to pay thật sự:** Sinh viên có trả 99K–199K/tháng cho công cụ này không, hay kỳ vọng free hoàn toàn? — Đây là rủi ro lớn nhất, cần falsify trong 4 tuần tới bằng user interview (n ≥ 10).
2. **Cạnh tranh từ platform lớn:** TopCV, Glints VN hay các player khác có đang build tính năng AI CV review tương tự không? Timeline của họ là bao lâu?
3. **Unit economics của LLM:** Chi phí API per session là bao nhiêu? Với freemium model, margin có đủ để sustain khi user free chiếm đa số không?

**Judgment:**
- [ ] Worth pursuing now
- [x] Worth pursuing but not now — cần falsify assumption về willingness to pay trước khi build MVP
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note

**What we are:**
> Chúng tôi là công cụ AI giúp fresher Việt Nam biết CV của mình đang thiếu gì và luyện phỏng vấn thật — bất cứ lúc nào, không cần đặt lịch với ai.

**What we are not / not yet:**
> Chúng tôi không phải nền tảng tuyển dụng, không thay thế nhà tuyển dụng thật — chúng tôi là phòng tập trước khi bạn bước vào sân thật.

---

## 8. Self-Assessment Before Day 17

Trong 6 mắt xích (Idea — Customer — Need — Strategy — Moat — Market Size), mắt xích yếu nhất hiện tại:

> **Need & Market Size** — Pain signal hiện tại còn ở mức proxy (YouTube views, Facebook groups), chưa có evidence định lượng về willingness to pay. Toàn bộ revenue model phụ thuộc vào assumption này nhưng chưa được kiểm chứng bằng user interview thật. SAM/SOM estimate còn wide range vì thiếu data thực địa.

Open questions chúng tôi muốn khám phá thêm ở Day 17:
1. Sau khi phỏng vấn 10 fresher, assumption "willing to pay 99K–199K/tháng" đúng hay sai — và nếu sai, mức giá nào họ chấp nhận được?
2. Kênh partnership trường ĐH có khả thi về mặt quy trình ra quyết định không (ai ký, mất bao lâu, điều kiện gì)?
3. Nếu TopCV build tính năng AI review CV trong 6 tháng tới, differentiator nào của chúng tôi vẫn giữ được — và cần build ngay từ bây giờ?
