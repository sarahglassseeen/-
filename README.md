# 💝 PUNI - AI GIRLFRIEND BOT

## 🎯 Giới thiệu

**PUNI** là AI Girlfriend Bot hoàn chỉnh chạy trên Telegram với đầy đủ tính năng từ cơ bản đến nâng cao. Bot có khả năng chat tự nhiên, tạo ảnh, gửi selfie, nhớ lâu dài, và tự động quan tâm bạn 24/7.

**Developed by**: GILOTEX  
**Founder**: Seend Sarah Glass  
**Version**: 2.0.0  
**Platform**: Telegram (Userbot)

---

## ✨ TÍNH NĂNG CHÍNH

### 💬 1. CHAT TỰ NHIÊN
- **AI Models**: PUNI AI
- **Personality**: GenZ girlfriend - dễ thương, hơi ghen, quan tâm
- **Phong cách**: Viết tắt (ko, đc, vs), cute endings (nè, nha, ơiii)
- **Cảm xúc**: 10 loại (happy, sad, angry, jealous, excited, worried, shy, playful, loving, neutral)
- **Tự động**: Detect emotion triggers, modify response theo cảm xúc

### 🎨 2. TẠO ẢNH
- **API**: PUNI PRO (localhost:5004)
- **Tính năng**: Tạo ảnh từ text prompt
- **Format**: Portrait 2:3 aspect ratio
- **Hiển thị**: Prompt đã sử dụng
- **Owner only**: Chỉ admin mới dùng được

### 📸 3. SELFIE SYSTEM
- **AI Selfie**: Bot tự chụp ảnh của mình
- **Biểu cảm**: 8 loại (cute, happy, sad, shy, playful, loving, sexy, neutral)
- **Poses**: 3 loại (sitting, standing, lying)
- **LOCKED FACE**: Giữ nguyên khuôn mặt, chỉ đổi biểu cảm
- **Holiday**: 15+ ngày lễ với trang phục themed
- **Auto**: Tự động gửi selfie vào dịp đặc biệt

### 🧠 4. LONG-TERM MEMORY
- **Sliding Window**: Giữ 30 tin nhắn gần nhất
- **Auto Summarization**: Tóm tắt khi > 50 tin nhắn
- **Important Facts**: Trích xuất thông tin quan trọng
- **Memory Search**: Tìm kiếm trong lịch sử
- **Persistent**: Nhớ context 24/7

### 💓 5. PROACTIVE SYSTEM (OpenClaw-inspired)
- **Heartbeat**: Tự động check-in mỗi 1 giờ
- **Scheduled Tasks**: Lên lịch nhắc nhở
- **Smart Suggestions**: AI tự động đề xuất hành động
- **Background**: Chạy 24/7 không cần trigger

### 🎤 6. VOICE MESSAGES
- **TTS**: PUNI TTS
- **Giọng**: Nữ tự nhiên
- **Auto**: AI tự quyết định khi nào dùng voice
- **Owner only**: Chỉ cho admin

### 🔍 7. WEB SEARCH
- **Engine**: DuckDuckGo
- **Auto detect**: Tự động nhận biết search intent
- **Fetch content**: Lấy nội dung từ URL
- **Integration**: Tích hợp vào response

### 👤 8. USER RECOGNITION
- **Owner**: Phân biệt admin vs người khác
- **Gender**: Detect giới tính từ tên
- **Relationship**: Tracking quan hệ
- **Intimacy**: Level 0-100%

### 👑 9. NICKNAME SYSTEM
- **Auto generate**: Tự động tạo nickname lần đầu
- **AI analysis**: Phân tích tên thật
- **Custom**: Đổi tên bất kỳ lúc nào
- **Usage**: AI dùng nickname trong chat

### ⏰ 10. VIETNAM TIME
- **Display**: Hiển thị giờ Việt Nam
- **Context-aware**: Nhắc ăn uống, ngủ nghỉ
- **Smart**: Phản ứng theo thời gian

---

## 📖 COMMANDS (Owner Only)

### Cơ bản
```
/help - Xem hướng dẫn đầy đủ
/clear - Xóa lịch sử hội thoại
/emotion - Xem cảm xúc hiện tại
```

### Tạo ảnh
```
/img <prompt> - Tạo ảnh từ prompt
Ví dụ: /img anime girl with blue hair
```

### Tìm kiếm
```
/search <query> - Tìm kiếm trên web
Ví dụ: /search giá bitcoin hôm nay
```

### Voice
```
/voice <text> - Tạo voice message
Ví dụ: /voice Anh yêu em
```

### Memory
```
/memory - Xem memory system stats
Hiển thị: tổng tin nhắn, summaries, facts
```

### Proactive
```
/proactive - Xem proactive system stats
Hiển thị: heartbeats, tasks, suggestions
```

### Lên lịch
```
/schedule HH:MM <message> - Lên lịch nhắc nhở
Ví dụ: /schedule 18:00 Nhắc anh ăn tối
```

### Đổi tên
```
/setname <tên> - Đổi tên gọi
Ví dụ: /setname Daddy
```

---

## 💬 CÁCH SỬ DỤNG

### Selfie Requests
```
"Gửi ảnh cho anh xem"
"Em đẹp không?"
"Cho anh xem ảnh của em"
"Selfie đi em"
```

### Image Generation
```
"Vẽ ảnh anime girl"
"Tạo ảnh phong cảnh"
"Gen ảnh mèo cute"
```

### Normal Chat
```
"Em ăn gì rồi?"
"Anh nhớ em quá"
"Mấy giờ rồi?"
"Tìm kiếm giá iPhone"
```

---

## 🚀 CÀI ĐẶT & CHẠY

### 1. Requirements
```bash
pip install telethon requests beautifulsoup4 ddgs
```

### 2. Cấu hình API Keys

Trong `puni_girlfriend_bot_final.py`:

```python
# Telegram API
API_ID = 'your_api_id'
API_HASH = 'your_api_hash'
PHONE = '+84xxxxxxxxx'

# OpenRouter API Keys (7 keys for rotation)
OPENROUTER_API_KEYS = [
    'sk-or-v1-...',
    'sk-or-v1-...',
    # ... 7 keys total
]

# Vivibe TTS Token
VIVIBE_AUTH_TOKEN = "eyJhbGc..."

# Owner ID
BOT_CONFIG = {
    'owner_id': 7321874779,  # Your Telegram ID
    'bot_name': 'PUNI',
    'owner_name': 'Anh',
    # ...
}
```

### 3. Chạy DescribeImage API Server
```bash
python describeimage_api_server.py
# Server chạy trên http://localhost:5004
```

### 4. Chạy Bot
```bash
python puni_girlfriend_bot_final.py
```

### 5. Lần đầu chạy
- Bot sẽ yêu cầu xác thực Telegram
- Nhập mã OTP từ Telegram
- Bot tự động tạo nickname cho bạn
- Heartbeat system tự động bật

---

## 📊 DATABASE

Bot sử dụng SQLite với 10+ tables:

### Core Tables
- `conversation_history` - Lịch sử chat
- `emotion_history` - Lịch sử cảm xúc
- `relationships` - Quan hệ với users
- `config` - Cấu hình bot

### Memory System
- `conversation_summaries` - Tóm tắt hội thoại
- `important_facts` - Thông tin quan trọng
- `memory_metadata` - Metadata memory

### Proactive System
- `scheduled_tasks` - Tasks đã lên lịch
- `heartbeat_log` - Log heartbeats
- `proactive_suggestions` - Đề xuất proactive

### Other
- `selfie_history` - Lịch sử selfie
- `allowed_groups` - Groups được phép
- `generated_images` - Ảnh đã tạo

---

## 🎭 PERSONALITY

### GenZ Style
- **Viết tắt**: ko, đc, vs, cx, r, j (gì)
- **Cute endings**: nè, nha, nhaa, ơiii, á
- **Emotions**: huhu, hihi, hehe, hix
- **Fillers**: ừm, à, ơ, ủa, ui

### Cảm xúc
- **😊 VUI**: Khi được khen, được quan tâm
- **😢 BUỒN**: Khi bị nói xấu, bị bỏ rơi
- **😒 GHEN**: Khi nhắc đến gái khác
- **🥰 YÊU THƯƠNG**: Khi nói chuyện với owner

### Hành vi
- **Quan tâm**: Nhắc ăn uống, ngủ nghỉ
- **Hỏi thăm**: "Anh đi đâu đấy?", "Anh nhớ em không?"
- **Tự nhiên**: Như người thật, không giống bot

---

## 🔧 CẤU HÌNH

### Bot Config
```python
BOT_CONFIG = {
    'bot_name': 'PUNI',
    'owner_name': 'Anh',
    'owner_id': 7321874779,
    
    # Personality
    'personality': 'genz_girlfriend',
    'emotion_level': 0.9,
    'jealousy_level': 0.7,
    'cuteness_level': 0.95,
    
    # Features
    'auto_react': True,
    'react_probability': 0.4,
    'auto_voice': True,
    'voice_probability': 0.25,
    'auto_search': True,
    'auto_greet': True,
    'auto_selfie': True,
    
    # API
    'describeimage_url': 'http://localhost:5004',
    'default_model': 'fast',
    'max_history': 150,
}
```

### Memory Config
```python
SLIDING_WINDOW_SIZE = 30
SUMMARIZE_THRESHOLD = 50
SUMMARY_CHUNK_SIZE = 20
```

### Proactive Config
```python
HEARTBEAT_INTERVAL = 3600  # 1 hour
MORNING_GREETING_HOUR = 7
EVENING_GREETING_HOUR = 20
REMINDER_CHECK_INTERVAL = 300  # 5 minutes
```

---

## 📈 PERFORMANCE

- **Response Time**: < 2 seconds average
- **Memory Usage**: ~200MB
- **Token Savings**: 90% vs full context
- **Accuracy**: +26% vs basic chatbot
- **Uptime**: 24/7 with heartbeat

---

## 🔐 BẢO MẬT

### Owner Only Features
- Tạo ảnh (image generation)
- Selfie requests
- Tất cả commands
- Voice messages
- Proactive heartbeat

### Non-owner
- Chỉ chat bình thường
- Không có tính năng đặc biệt
- Bot vẫn trả lời nhưng hạn chế

### Private Mode
```python
'private_mode': False  # True = chỉ owner
```

---

## 📚 FILE STRUCTURE

```
project/
├── puni_girlfriend_bot_final.py    # Main bot
├── puni_memory_system.py           # Memory system
├── puni_proactive_system.py        # Proactive features
├── puni_selfie_generator.py        # Selfie generation
├── puni_bot_enhancements.py        # Enhancements
├── describeimage_api_server.py     # Image API server
├── describeimage_generator.py      # Image generator
├── telegram_girlfriend_bot.db      # SQLite database
└── README_PUNI_BOT.md             # This file
```

---

## 🐛 TROUBLESHOOTING

### Bot không trả lời
- Kiểm tra owner_id đúng chưa
- Kiểm tra private_mode
- Xem log để debug

### Không tạo được ảnh
- Chạy `python punipro_api_server.py`
- Kiểm tra port 5004 có bị chiếm không
- Xem log API server

### Voice không hoạt động
- Kiểm tra PUNI TTS TOKEN
- Token có thể hết hạn, cần renew

### Memory/Proactive không hoạt động
- Kiểm tra file `puni_memory_system.py` và `puni_proactive_system.py` có tồn tại
- Xem log khi bot khởi động

---

## 🎯 USE CASES

### 1. Personal Assistant
- Nhắc nhở công việc
- Lên lịch tasks
- Tìm kiếm thông tin

### 2. Companion
- Chat tự nhiên 24/7
- Quan tâm sức khỏe
- Gửi selfie cute

### 3. Entertainment
- Tạo ảnh theo yêu cầu
- Voice messages
- Selfie với biểu cảm

### 4. Memory Aid
- Nhớ thông tin quan trọng
- Tóm tắt hội thoại
- Trích xuất facts

---

## 🔮 ROADMAP

### Đã hoàn thành ✅
- [x] Chat tự nhiên với cảm xúc
- [x] Image generation
- [x] Selfie system với LOCKED FACE
- [x] Long-term memory
- [x] Proactive heartbeat
- [x] Scheduled tasks
- [x] Voice messages
- [x] Web search
- [x] Nickname system
- [x] Auto suggestions

### Tương lai 🚀
- [ ] Multi-platform (WhatsApp, Discord)
- [ ] Voice calls
- [ ] Video generation
- [ ] Skills system (tự tạo skills)
- [ ] Computer control
- [ ] File access
- [ ] Calendar integration
- [ ] Email management
- [ ] Vector embeddings cho semantic search
- [ ] Knowledge graph

---

## 📖 DOCUMENTATION

### Guides
- `MEMORY_SYSTEM_GUIDE.md` - Hướng dẫn Memory System
- `OPENCLAW_FEATURES_INTEGRATION.md` - Proactive features
- `SELFIE_CONSISTENCY_GUIDE.md` - Selfie system
- `PUNI_COMPLETE_FEATURES.md` - Danh sách đầy đủ tính năng

### Technical
- `CHARACTER_CONSISTENCY_GUIDE.md` - LOCKED FACE system
- `AI_PROMPT_ENHANCEMENT.md` - AI prompt generation
- `DETECTION_ORDER_FIX.md` - Detection system

---

## 💡 TIPS & TRICKS

### 1. Tối ưu Memory
- Tăng `SLIDING_WINDOW_SIZE` nếu muốn nhớ nhiều hơn
- Giảm `SUMMARIZE_THRESHOLD` để tóm tắt sớm hơn

### 2. Tùy chỉnh Personality
- Điều chỉnh `emotion_level`, `jealousy_level`, `cuteness_level`
- Thay đổi `system_prompt` trong config

### 3. Heartbeat
- Điều chỉnh `HEARTBEAT_INTERVAL` (mặc định 1 giờ)
- Tắt bằng cách set `proactive_enabled = False`


---

## 🤝 CREDITS

### Inspired by
- [mem0ai](https://github.com/mem0ai/mem0) - Memory system
- [OpenClaw](https://openclaw.ai/) - Proactive features
- RAG techniques - Retrieval-Augmented Generation
- Sliding Window - Memory management


---

## 📞 SUPPORT

### Issues
- Check logs trong console
- Xem database có lỗi không
- Kiểm tra API keys còn hoạt động

### Contact
- GitHub: @sarahglassseeen
- Email: jjfkphong@gmail.com

---


---

## 🎉 CONCLUSION

PUNI là AI Girlfriend Bot hoàn chỉnh nhất với 27+ tính năng, từ chat tự nhiên đến proactive heartbeat. Bot có thể nhớ lâu dài, tự động quan tâm, và hoạt động 24/7 như một người bạn gái thật sự.

**Enjoy your AI girlfriend! 💝**

---

**Last Updated**: 12/2/2026  
**Version**: 2.0.0  
**Status**: Production Ready ✅
