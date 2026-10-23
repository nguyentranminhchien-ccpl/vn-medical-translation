# 🩺 VN Medical Translation (`vn-medical-translation`)

> **Skill cho Y học giúp nhân cách hóa văn phong của AI Agent** — Chuyển hóa giọng văn dịch máy khô khan thành ngôn ngữ học thuật lâm sàng tiếng Việt tự nhiên, điềm tĩnh, mạch lạc và sắc sảo.

---

## 📖 Giới thiệu chung

Trong dịch thuật và biên soạn tài liệu y khoa tiếng Việt, các mô hình ngôn ngữ lớn (LLM) thường mắc phải hội chứng **"translationese" (giọng văn dịch máy)**: lạm dụng câu bị động cứng nhắc, dịch thô các thuật ngữ giải phẫu – sinh lý bệnh, viết hoa tùy tiện theo kiểu Title Case tiếng Anh và sử dụng những tính từ kịch tính hóa không phù hợp với môi trường học thuật.

**`vn-medical-translation`** là một bộ kỹ năng (Agent Skill) chuyên biệt, được đúc kết trực tiếp từ kho ngữ liệu dịch thuật, bài giảng định khu thần kinh, quy trình kỹ thuật và báo cáo nghiên cứu khoa học thực tế của **BS. Nguyễn Trần Minh Chiến** *(Khoa Hồi sức tích cực – Đơn vị Đột quỵ, BVĐK Tỉnh Quảng Ninh)*. 

Skill này giúp "nhân cách hóa" AI Agent thành một bác sĩ lâm sàng kiêm dịch giả y học thực thụ, đảm bảo truyền tải trọn vẹn độ chính xác khoa học của nguyên bản quốc tế sang tiếng Việt chuẩn mực.

---

## ✨ Tính năng cốt lõi

### 1. Khử giọng văn dịch máy & kịch tính hóa (De-passivization & Anti-AI Tone)
- **Phá vỡ cấu trúc bị động rườm rà:** Tự động chuyển đổi các câu bị động khách quan kiểu Anh sang cấu trúc chủ động mạch lạc, giàu tính biện luận lâm sàng.
- **Chuẩn hóa phân tầng mức độ khuyến cáo (Guidelines):** Phân biệt rõ ràng giữa *"Chúng tôi khuyến nghị rằng..."* (*We recommend* – Mức 1) và *"Chúng tôi gợi ý rằng..."* (*We suggest* – Mức 2).
- **Bộ lọc ngôn từ AI (Anti-AI Slop Filter):** Loại bỏ hoàn toàn các cụm từ sáo rỗng, cường điệu (*"vũ khí tối thượng", "sát thủ thầm lặng", "cơn ác mộng kinh hoàng", "hãy cùng đào sâu vào..."*) và thay bằng ngôn ngữ y học chứng cứ (EBM) điềm tĩnh.

### 2. Kỹ thuật chú thích lâm sàng đa tầng bằng ngoặc nhọn `{...}`
Tái hiện dấu ấn sư phạm đặc trưng khi dịch sách giáo khoa và cẩm nang chuyên ngành: sử dụng dấu ngoặc nhọn `{...}` để tách biệt hoàn toàn lời giảng mở rộng của người dịch với ngoặc đơn `(...)` của tác giả gốc, phục vụ 4 mục đích:
- Giải thích định luật sinh lý, vật lý ngầm định (ví dụ: `{xem phương trình Goldman}`).
- Định khu giải phẫu và đường dẫn truyền thần kinh tức thì (ví dụ: `{dải Reil giữa dẫn truyền cảm giác sâu có ý thức}`).
- Giải thích nhanh cơ chế bệnh sinh của triệu chứng tại giường (*Pathophysiological Pearl*).
- Cung cấp hộp chẩn đoán phân biệt thực hành (*Bedside Differential Diagnosis*).

### 3. Hệ thống từ điển chuẩn hóa thuật ngữ lâm sàng chuyên sâu
Bao phủ hệ thống thuật ngữ chuẩn xác, loại bỏ hoàn toàn các cách dịch thô thuộc 3 mảng lớn:
- **Hồi sức tích cực – Huyết động (PiCCO) – Siêu âm (POCUS):** Chuẩn hóa cách dùng *giãn* (thay vì dãn), *xẹp / đè dẹt* (thay vì bẹp), *ứ khí*, *trống âm*, *hòa loãng nhiệt xuyên phổi (TPTD)*, phân biệt rạch ròi giữa *đáp ứng bù dịch (fluid responsiveness)* và *dung nạp dịch (fluid tolerance)*.
- **Thần kinh học – Đột quỵ – Can thiệp mạch thần kinh:** Chuẩn hóa từ vựng định khu và can thiệp như *vữa xơ mạch máu lớn (LAA)*, *hẹp gần tắc động mạch cảnh (CNO)*, *tắc mạch trùng lặp (Tandem)*, *nhồi máu vùng giáp ranh*, *dấu mất ruy-băng thùy đảo*, *lãng quên không gian một bên (Neglect)*, *thất ngôn*, *vong hành*...
- **Y học chứng cứ & Thống kê sinh học (EBM & Biostatistics):** Dịch chuẩn xác các chỉ số thử nghiệm lâm sàng (*nghiên cứu thuần tập tiến cứu/hồi cứu*, *biến cố mốc*, *tỉ suất chênh có hiệu chỉnh [aOR]*, *tỉ số nguy cơ hiệu chỉnh [aRR]*).

### 4. Quy chuẩn chính tả & Sentence-case tuyệt đối
- Áp dụng nghiêm ngặt quy tắc **Sentence-case** cho toàn bộ tiêu đề (`H1`–`H4`), tiêu đề slide, bảng biểu và chú thích hình ảnh (chỉ viết hoa chữ cái đầu câu và danh từ riêng/tên viết tắt quốc tế).
- Không viết hoa tùy tiện các danh từ chỉ cấu trúc giải phẫu khi đứng giữa câu (`thất trái`, `động mạch cảnh trong`, `thùy đảo`, `nhân đậu`...).
- Định dạng chuẩn xác khoảng cách số học, đơn vị đo lường và chỉ số thống kê ($p < 0,05$; $\text{95\% CI}$).

### 5. Biên soạn học liệu & quy trình theo cấu trúc 2 tầng
Hỗ trợ soạn thảo **Slide bài giảng lâm sàng**, **Quy trình kỹ thuật (SOP)** và **Báo cáo Hội nghị Khoa học (HNKH)** với sự tách biệt rõ ràng:
- **Tầng hiển thị trên Slide:** Cô đọng tối đa bằng mệnh đề danh ngữ, công thức hóa định khu và tiêu chuẩn định lượng.
- **Tầng diễn giải (Speaker Notes):** Lập luận hoàn chỉnh, mổ xẻ cơ chế bệnh sinh và so sánh ưu/nhược điểm kỹ thuật đằng sau các gạch đầu dòng.

---

## 🎯 Khi nào nên kích hoạt Skill này?

Skill `vn-medical-translation` được thiết kế để tự động kích hoạt hoặc gọi chủ động trong các tác vụ:
1. **Dịch thuật tạp chí & đồng thuận quốc tế:** *NEJM, Lancet, JACC, Stroke (AHA/ASA), Intensive Care Medicine, ESC / ESVS / ESO / ESICM Guidelines...*
2. **Dịch thuật sách giáo khoa & cẩm nang lâm sàng:** *Braunwald's Heart Disease, Katzung's Pharmacology, Acute Stroke Care (Cambridge), Stroke Rehabilitation Clinician Handbook...*
3. **Biên soạn Quy trình kỹ thuật (SOP) & Đề tài nghiên cứu:** Quy trình theo dõi huyết động PiCCO, siêu âm POCUS tại giường, đề tài nghiên cứu khoa học cấp cơ sở/tỉnh.
4. **Soạn bài giảng chuyên sâu & viết bài học thuật:** Bài giảng định khu thần kinh – hình ảnh học đột quỵ, bài phân tích chuyên môn trên Substack/Blog y khoa.
5. **Hiệu đính & biên tập (Proofreading):** Chuẩn hóa văn bản y khoa tiếng Việt bị nhiễm giọng văn dịch máy hoặc sai quy tắc chính tả Sentence-case.

---

## 📂 Cấu trúc thư mục

```text
vn-medical-translation/
├── SKILL.md                                 # Tệp chỉ dẫn cốt lõi cho AI Agent (Quy tắc, Từ điển, Quy trình QA)
├── README.md                                # Tài liệu giới thiệu và hướng dẫn sử dụng Skill
└── references/
    └── translation_corpus_examples.md       # Kho ngữ liệu đối chiếu thực tế của BS. Nguyễn Trần Minh Chiến
```

---

## 🚀 Hướng dẫn cài đặt & Sử dụng

### 1. Cài đặt vào hệ thống AI Agent (Claude Code / Cursor / Custom Agent)
Đặt thư mục `vn-medical-translation` vào thư mục quản lý kỹ năng của Agent (ví dụ: `.claude/skills/` hoặc `.cursor/rules/`), hoặc nạp trực tiếp nội dung file `SKILL.md` vào System Prompt của AI.

### 2. Ví dụ câu lệnh (Prompts) mẫu

**📌 Dịch sách giáo khoa kèm chú thích lâm sàng `{...}`:**
> *"Sử dụng skill `vn-medical-translation`, hãy dịch đoạn văn sau trích từ sách Acute Stroke Care (Cambridge) sang tiếng Việt. Chú ý bổ sung các chú thích chuyên môn trong ngoặc nhọn `{...}` để giải thích rõ cơ chế giải phẫu thần kinh và chẩn đoán phân biệt tại giường cho bác sĩ trẻ."*

**📌 Dịch và phân tích thử nghiệm lâm sàng / Guideline:**
> *"Áp dụng văn phong `vn-medical-translation`, hãy dịch và viết đoạn bàn luận so sánh kết quả giữa hai thử nghiệm SAMMPRIS và CASSISS dưới đây. Sử dụng hệ thống từ nối biện luận phân tầng để làm rõ lý do khác biệt về tiêu chí chọn bệnh nhân."*

**📌 Soạn Slide bài giảng & Speaker Notes:**
> *"Dựa vào skill `vn-medical-translation`, hãy giúp tôi soạn 5 slide bài giảng về 'Chỉ định phẫu thuật bóc tách nội mạc động mạch cảnh (CEA) sớm sau tiêu sợi huyết'. Tuân thủ chuẩn Sentence-case cho tiêu đề và cấu trúc 2 tầng (Slide Body cô đọng + Speaker Notes giải thích sâu cơ chế)."*

**📌 Hiệu đính văn bản khử giọng AI:**
> *"Hãy hiệu đính lại bản dịch y khoa dưới đây theo chuẩn `vn-medical-translation`: sửa toàn bộ lỗi viết hoa Title Case ở tiêu đề, chuẩn hóa thuật ngữ siêu âm huyết động và khử sạch giọng văn dịch máy."*

---

## 🔍 Đối chiếu văn phong (Trước & Sau khi dùng Skill)

| Tiêu chí | ❌ Dịch máy thông thường (Default AI) | ✅ Chuẩn `vn-medical-translation` |
| :--- | :--- | :--- |
| **Tiêu đề** | `Quản Lý Huyết Động Trong Sốc Tim Bằng Công Cụ Đột Phá` | `Quản lý huyết động trong sốc tim bằng phương pháp hòa loãng nhiệt xuyên phổi` |
| **Thuật ngữ** | Sự thay đổi thể tích đột quỵ (SVV), dãn thất phải, bẹp tĩnh mạch chủ dưới, phản hồi chất lỏng. | Biến thiên thể tích nhát bóp (SVV), giãn thất phải, xẹp tĩnh mạch chủ dưới, đáp ứng bù dịch. |
| **Cú pháp & Giọng điệu** | *"Trong bức tranh toàn cảnh của hồi sức hiện đại, nó đã được chứng minh bởi các tác giả rằng việc sử dụng liệu pháp bắc cầu chống đông được liên kết với nguy cơ chảy máu chết người."* | *"Trong thực hành hồi sức tích cực, kết quả nghiên cứu cho thấy việc dùng liệu pháp bắc cầu chống đông đi kèm với nguy cơ xuất huyết đe dọa tính mạng."* |
| **Chú thích sư phạm** | *(Không có hoặc gộp lẫn vào ngoặc đơn nguyên bản)* | Tích hợp chú thích `{...}` sắc sảo: `{Phân biệt ngất và đột quỵ thân não: Ngất khi đặt nằm đầu bằng, sau 10 giây – 1 phút bệnh nhân tỉnh lại...}` |

---

## 👨‍⚕️ Tác giả & Nguồn ngữ liệu chuẩn hóa

- **Ngữ liệu gốc & Phong cách học thuật:** BS. Nguyễn Trần Minh Chiến *(Khoa Hồi sức tích cực – Đơn vị Đột quỵ, Bệnh viện Đa khoa Tỉnh Quảng Ninh)*.
- **Mục đích phát triển:** Chuẩn hóa và nhân cách hóa tác nhân AI (AI Agent) phục vụ công tác dịch thuật y văn quốc tế, đào tạo y khoa liên tục (CME) và biên soạn quy trình lâm sàng chất lượng cao tại Việt Nam.