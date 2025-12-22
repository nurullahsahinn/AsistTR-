# 🇹🇷 AsistTR Canlı Destek Platformu

<div align="center">

**Tawk.to benzeri, RAG teknolojisi ile güçlendirilmiş, self-hosted canlı destek ve ticket yönetim platformu**

[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![WebRTC](https://img.shields.io/badge/WebRTC-Enabled-333333?logo=webrtc)](https://webrtc.org/)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

[Dokümantasyon](#-dokümantasyon) · [Özellikler](#-özellikler) · [Kurulum](#-hızlı-başlangıç) · [Demo](#)

</div>

---

## 🎯 Proje Hakkında

**AsistTR**, web sitelerine gömülebilir bir sohbet widget'ı ile ziyaretçilerle **gerçek zamanlı** iletişim kurmayı, **sesli arama** yapmayı, **yapay zeka destekli** otomatik yanıtlar vermeyi ve **ticket yönetim sistemi** sunmayı sağlayan **tamamen açık kaynaklı** ve **self-hosted** bir platformdur.

### 🏆 Ana Özellikler

- ✅ **Gerçek Zamanlı Mesajlaşma** - WebSocket ile anlık iletişim
- ✅ **AI Destekli Yanıtlar** - RAG teknolojisi ile akıllı otomatik cevaplar (Ollama)
- ✅ **Sesli Arama** - WebRTC ile P2P sesli görüşme
- ✅ **Ticket Sistemi** - osTicket benzeri gelişmiş ticket yönetimi
- ✅ **Kanban Board** - Ticket'ları görsel olarak yönetme
- ✅ **Dynamic Forms** - Özelleştirilebilir form oluşturma
- ✅ **Email Entegrasyonu** - SMTP ile otomatik email bildirimleri
- ✅ **Çoklu Agent Desteği** - Sınırsız agent ekleme ve yönetimi
- ✅ **Akıllı Routing** - 6 farklı routing stratejisi
- ✅ **Analytics & Raporlama** - Detaylı istatistikler ve metrikler
- ✅ **Ziyaretçi Takibi** - Sayfa görüntüleme, heatmap, funnel analizi

---

## ✨ Özellikler

### 💬 Mesajlaşma & İletişim

- **Gerçek Zamanlı Mesajlaşma**: WebSocket ile anlık iletişim
- **Sesli Arama (WebRTC)**: Widget'tan doğrudan sesli arama başlatma + P2P bağlantı
- **Typing Indicators**: Karşı tarafın yazma durumunu gösterme
- **Mesaj Geçmişi**: Tüm konuşmalar veritabanında saklanır
- **Dosya Gönderimi**: Resim ve belge paylaşımı
- **Session Continuity**: Returning visitor için sohbet devam ettirme
- **Grup Görünümü**: Aynı ziyaretçinin tüm sohbetlerini tek başlık altında toplama
- **Dahili Notlar**: Agent'lar arası gizli notlar (müşteri görmez)
- **Chat Transfer**: Sohbeti başka agent'a aktarma
- **Etiketleme**: Konuşmalara tag ekleme ve filtreleme
- **Markdown Desteği**: Mesajlarda markdown formatı desteği
- **Streaming Yanıtlar**: ChatGPT benzeri karakter karakter metin görüntüleme

### 🤖 AI & RAG Sistemi

- **AI Destekli Yanıtlar**: RAG teknolojisi ile akıllı otomatik cevaplar
- **Streaming Yanıtlar**: ChatGPT benzeri karakter karakter metin görüntüleme
- **AI Kontrol**: Agent AI'ı durdurabilir/devam ettirebilir
- **Markdown Desteği**: Başlıklar, listeler, kalın/italik metin renderı
- **Hibrit Arama**: Text-based + Vector-based bilgi alma
- **pgvector + HNSW Index**: Yüksek performanslı vector search
- **Context-Aware**: Konuşma geçmişini anlayan akıllı yanıtlar
- **Local LLM**: Ollama ile tamamen offline çalışma (llama3.1:8b)

### 🎫 Ticket Yönetim Sistemi

- **Modern Ticket Sistemi**: osTicket benzeri profesyonel ticket yönetimi
- **Kanban Board**: Ticket'ları görsel olarak yönetme (Yeni, Açık, Çözüldü, Kapatıldı)
- **Ticket Şablonları**: Hazır ticket şablonları ile hızlı yanıt verme
- **Ticket Filtreleri**: Gelişmiş filtreleme ve arama
- **Priority Seviyeleri**: Düşük, Normal, Yüksek, Acil
- **Status Yönetimi**: Yeni, Açık, Yanıt Bekleniyor, Çözüldü, Kapatıldı
- **Ticket Kategorileri**: Kategori bazlı organizasyon
- **Ticket Kilitleme**: Aynı anda birden fazla agent'ın düzenlemesini engelleme
- **Ticket Geçmişi**: Tam audit trail
- **Custom Fields**: Özel alanlar ekleme

### 📝 Dynamic Forms (Dinamik Formlar)

- **Form Builder**: Drag & drop ile kolay form oluşturma
- **Field Types**: Text, Textarea, Select, Radio, Checkbox, Date, Email, Phone, File Upload
- **Conditional Logic**: Koşullu alan gösterimi
- **Form Validation**: Gelişmiş validasyon kuralları
- **Form Templates**: Hazır form şablonları
- **Submission Tracking**: Form gönderimlerini takip etme
- **Ticket Integration**: Form gönderimlerini otomatik ticket'a dönüştürme

### 👥 Agent Yönetimi

- **Çoklu Agent Desteği**: Sınırsız agent ekleyebilme
- **Agent Durumları**: Müsait, Uzakta, Meşgul, Molada, Rahatsız Etmeyin, Çevrimdışı
- **Departman Yönetimi**: Agent'ları departmanlara atama
- **Skill-Based Routing**: Yeteneklere göre akıllı yönlendirme
- **Agent Call Availability**: Sesli arama kabul etme durumu
- **Canned Responses**: Hazır yanıt şablonları
- **Grace Period**: Bağlantı koptuğunda 60sn yeniden bağlanma süresi
- **Durum Senkronizasyonu**: Sidebar ve yönetim sayfası otomatik güncellenir
- **Team Management**: Ekip oluşturma ve yönetimi
- **Agent Performance Metrics**: İlk yanıt süresi, ortalama yanıt süresi, çözüm süresi

### 🎯 Routing & Queue

- **Round Robin**: Sıralı agent dağıtımı
- **Least Busy**: En az meşgul agent'a yönlendirme
- **Department Routing**: Departman bazlı yönlendirme
- **Skill-Based Routing**: Yeteneklere göre yönlendirme
- **VIP Routing**: VIP müşterilere öncelik
- **Language-Based Routing**: Dillere göre yönlendirme
- **Call Queue**: Müşteri bekleme kuyruğu
- **Queue Position Tracking**: Kuyruk sırası takibi
- **Estimated Wait Time**: Tahmini bekleme süresi hesaplama

### 🔔 Bildirimler & Analytics

- **Real-time Notifications**: Yeni mesaj ve arama bildirimleri
- **Desktop Notifications**: Tarayıcı bildirimleri (Web Push API)
- **Notification Preferences**: Kişiselleştirilebilir bildirim ayarları
- **Canlı Ziyaretçi İzleme**: Anlık ziyaretçi listesi (Tawk.to benzeri)
- **Visitor Timeline**: Ziyaretçi gezinti geçmişi + heatmap analizi
- **Funnel Analysis**: Giriş/çıkış sayfaları, drop-off point tespiti
- **Page View Tracking**: Sayfa görüntüleme ve davranış takibi
- **Agent Performans Metrikleri**: İlk yanıt, ortalama yanıt, çözüm süresi
- **CSAT & Rating**: Müşteri memnuniyeti puanlama sistemi
- **Conversation Analytics**: Çözüm oranı, rating dağılımı, saatlik istatistikler
- **Kuyruk Monitörü**: Bekleyen müşteri sayısı, ortalama bekleme süresi

### 📧 Email Entegrasyonu

- **SMTP Desteği**: Gmail, Outlook, özel SMTP sunucuları
- **Auto-Responder**: Otomatik yanıt email'leri
- **Email Templates**: Özelleştirilebilir email şablonları
- **Ticket Notifications**: Ticket oluşturma/güncelleme bildirimleri
- **Email Settings**: Gelişmiş email yapılandırması
- **Email Parsing**: Gelen email'leri parse etme ve ticket'a dönüştürme (IMAP)

### 🎨 Widget & Özelleştirme

- **Proactive Chat**: Otomatik sohbet başlatma (time, scroll, idle, visibility triggers)
- **Customizable Widget**: Renk, pozisyon, mesaj özelleştirme
- **Kolay Entegrasyon**: Tek satır kod ile web sitenize ekleyin
- **Responsive Design**: Mobil uyumlu tasarım
- **Offline Mesaj Formu**: Agent yokken mesaj bırakma
- **Widget API**: JavaScript API ile programatik kontrol
- **Auto-expand**: İlk yüklenmede otomatik açma seçeneği
- **Custom CSS**: Özel CSS ile widget'ı tamamen özelleştirme

### 📊 Dashboard & UI

- **Modern React Dashboard**: React 18 + Vite + Tailwind CSS
- **Real-time Updates**: Socket.IO ile anlık güncellemeler
- **Responsive Design**: Mobil, tablet ve desktop uyumlu
- **Dark Mode Ready**: Karanlık mod desteği (gelecek özellik)
- **Performance Metrics**: Gerçek zamanlı performans metrikleri
- **Kanban Board**: Ticket'ları görsel olarak yönetme
- **Customer Management**: Müşteri bilgilerini yönetme
- **Knowledge Base Management**: Bilgi tabanı yönetimi

### 🔐 Güvenlik & Yönetim

- **JWT Tabanlı Auth**: Güvenli kimlik doğrulama
- **Role-Based Access**: Admin/Agent rol yönetimi
- **Multi-Site Support**: Tek platformda çoklu site yönetimi
- **API Key Management**: Site bazlı API key kontrolü
- **Rate Limiting**: DDoS koruması
- **Input Sanitization**: XSS koruması
- **SQL Injection Protection**: Parameterized queries
- **CORS Policy**: Whitelisted domains
- **HTTPS/WSS Support**: Production için güvenli bağlantı

---

## 🏗️ Mimari

```
┌─────────────────────────────────────────────────────────────┐
│                      CLIENT LAYER                            │
├─────────────────────────────────────────────────────────────┤
│  Widget (Ziyaretçi)          Dashboard (Admin)              │
│  - Vanilla JS                - React 18 + Vite              │
│  - Socket.IO Client          - Zustand (State)              │
│  - Embedded Script           - React Router                 │
└──────────────────┬──────────────────────────┬───────────────┘
                   │                          │
                   ▼                          ▼
┌─────────────────────────────────────────────────────────────┐
│                  APPLICATION LAYER                           │
├─────────────────────────────────────────────────────────────┤
│                    Backend (Node.js)                         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │   REST API   │  │   Socket.IO  │  │  RAG Engine  │      │
│  │  (Express)   │  │  (WebSocket) │  │   (Ollama)   │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐  │
│  │              Middleware Layer                        │  │
│  │  - Auth (JWT)  - Validation  - Rate Limiting        │  │
│  └──────────────────────────────────────────────────────┘  │
└──────────────────┬──────────────────────────┬───────────────┘
                   │                          │
                   ▼                          ▼
┌─────────────────────────────────────────────────────────────┐
│                        DATA LAYER                            │
├─────────────────────────────────────────────────────────────┤
│   PostgreSQL              Redis              Ollama          │
│   - Conversations         - Cache            - LLM           │
│   - Messages             - Pub/Sub          - Embeddings    │
│   - Tickets              - Sessions                          │
│   - Users                - Presence                          │
│   - Knowledge Base       - Queue                             │
│   - pgvector (HNSW)                                         │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Teknoloji Yığını

| Katman | Teknoloji |
|--------|-----------|
| **Frontend Dashboard** | React 18 + Vite 5 + Tailwind CSS 3 |
| **Frontend Widget** | Vanilla JavaScript + Socket.IO Client |
| **Backend** | Node.js 18+ + Express 4 + Socket.IO 4 |
| **Database** | PostgreSQL 15 + pgvector |
| **Cache** | Redis 7 |
| **RAG** | LangChain + pgvector (HNSW index) |
| **LLM** | Ollama (llama3.1:8b) - Local |
| **Embedding** | nomic-embed-text (768 dimensions) |
| **Voice** | WebRTC (Peer-to-Peer) |
| **Auth** | JWT + bcrypt |
| **Email** | Nodemailer + IMAP |
| **Deployment** | Docker 24+ + Docker Compose 2 |
| **Real-time** | WebSocket / Socket.IO |

---

## 📁 Proje Yapısı

```
AsistTR/
├── backend/                    # Node.js API sunucusu
│   ├── src/
│   │   ├── controllers/        # API controller'lar (29 dosya)
│   │   │   ├── agent.controller.js
│   │   │   ├── ticket.controller.js
│   │   │   ├── chat.controller.js
│   │   │   ├── email.controller.js
│   │   │   └── ...
│   │   ├── models/             # Veritabanı modelleri
│   │   │   ├── Ticket.model.js
│   │   │   ├── DynamicForm.model.js
│   │   │   └── ...
│   │   ├── routes/             # API route'lar (29 dosya)
│   │   ├── services/           # İş mantığı servisleri (11 dosya)
│   │   ├── middleware/         # Auth, validation vb.
│   │   ├── socket/             # WebSocket handlers (11 dosya)
│   │   │   ├── handlers/
│   │   │   │   ├── message.handler.js
│   │   │   │   ├── voiceCall.handler.js
│   │   │   │   └── ...
│   │   │   └── setup.js
│   │   ├── rag/                # RAG pipeline (3 dosya)
│   │   └── utils/              # Yardımcı fonksiyonlar (11 dosya)
│   ├── migrations/             # Veritabanı migration'ları
│   ├── app.js                  # Ana uygulama dosyası
│   └── package.json
│
├── frontend/
│   ├── dashboard/              # React Admin Dashboard
│   │   ├── src/
│   │   │   ├── pages/          # Sayfalar (20+ dosya)
│   │   │   │   ├── ChatPage.jsx
│   │   │   │   ├── TicketsPage.jsx
│   │   │   │   ├── AnalyticsPage.jsx
│   │   │   │   └── ...
│   │   │   ├── components/     # Bileşenler (15+ dosya)
│   │   │   │   ├── TicketKanban.jsx
│   │   │   │   ├── VoiceCallPanel.jsx
│   │   │   │   └── ...
│   │   │   ├── services/       # API servisleri
│   │   │   └── store/          # Zustand state management
│   │   └── package.json
│   │
│   └── widget/                 # Ziyaretçi sohbet widget'ı
│       ├── src/                # 22 JavaScript dosyası
│       └── package.json
│
├── docs/                       # Dokümantasyon
│   ├── ARCHITECTURE.md
│   ├── API.md
│   ├── KURULUM.md
│   └── FAQ.md
│
├── docker-compose.yml          # Docker Compose yapılandırması
├── .env.example                # Environment variables örneği
└── README.md                   # Bu dosya
```

---

## 🚀 Hızlı Başlangıç

### Gereksinimler

- Docker 24+
- Docker Compose 2.20+
- 8GB RAM (minimum, Ollama için)
- 20GB Disk Alanı (Ollama modeli için)
- Ollama model indirmesi için internet bağlantısı (ilk kurulum)

### Kurulum Adımları

1. **Repository'yi klonlayın**
```bash
git clone https://github.com/nurullahsahinn/AsistTR.git
cd AsistTR
```

2. **Environment variables'ı ayarlayın**
```bash
# Backend için .env dosyası oluşturun
cp backend/.env.example backend/.env

# Önemli ayarları düzenleyin:
# - JWT_SECRET (minimum 32 karakter)
# - SMTP ayarları (email için)
# - OPENAI_API_KEY (opsiyonel)
```

3. **Docker container'ları başlatın**
```bash
docker-compose up -d
```

4. **Ollama modelini yükleyin** (ÖNEMLİ!)
```bash
# Ollama container'ına bağlanın
docker exec -it asistr_ollama ollama pull llama3.1:8b

# Embedding modelini yükleyin
docker exec -it asistr_ollama ollama pull nomic-embed-text:latest

# Model listesini kontrol edin
docker exec -it asistr_ollama ollama list
```

5. **Veritabanı migration'larını çalıştırın**
```bash
# Tüm migration'ları çalıştır (önerilen)
docker exec -i asistr_backend node run-all-migrations.js

# VEYA sadece ana migration (eski yöntem)
docker exec -i asistr_backend node src/utils/migrate.js
```

6. **Vector index'ini oluşturun**
```bash
docker exec -i asistr_backend node src/utils/create-vector-index.js
```

7. **İlk admin kullanıcısını oluşturun**
```bash
# Backend container'ına bağlanın
docker exec -it asistr_backend sh

# Seed script'i çalıştırın (opsiyonel)
node src/utils/seed.js
```

8. **Servisleri kontrol edin**
```bash
# Tüm container'ların çalıştığını kontrol edin
docker ps

# Backend loglarını kontrol edin
docker logs -f asistr_backend

# Ollama servisini test edin
curl http://localhost:11434/api/tags
```

### Servislere Erişim

- **Dashboard**: http://localhost:3000
- **Widget**: http://localhost:5173
- **Backend API**: http://localhost:4000/api
- **WebSocket**: ws://localhost:4000
- **PostgreSQL**: localhost:5432
- **Redis**: localhost:6379
- **Ollama**: http://localhost:11434

---

## 📖 Kullanım

### Widget Entegrasyonu

1. **Dashboard'dan API Key alın**
   - http://localhost:3000 adresine giriş yapın
   - Widget Settings sayfasından API Key'inizi kopyalayın

2. **Web sitenize kodu ekleyin**

#### Development (Localhost)
```html
<script>
(function(){
  window.AsistTRConfig = {
    apiKey: 'YOUR_API_KEY_HERE',
    apiUrl: 'http://localhost:4000',
    wsUrl: 'ws://localhost:4000'
  };
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = 'http://localhost:5173/widget.js';
  var x = document.getElementsByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();
</script>
```

#### Production (Canlı Ortam)
```html
<script>
(function(){
  window.AsistTRConfig = {
    apiKey: 'YOUR_API_KEY_HERE'
    // apiUrl ve wsUrl belirtilmezse otomatik olarak script'in geldiği domain kullanılır
  };
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = 'https://chat.asisttr.com/widget.js';  // Production widget URL
  var x = document.getElementsByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();
</script>
```

3. **Özelleştirme (Opsiyonel)**
```html
<script>
window.AsistTRConfig = {
  apiKey: 'YOUR_API_KEY_HERE',
  primaryColor: '#4F46E5',
  position: 'right', // 'left' or 'right'
  welcomeMessage: 'Merhaba! Size nasıl yardımcı olabilirim?',
  agentName: 'Destek Ekibi',
  proactiveChat: {
    enabled: true,
    timeOnPage: 30, // saniye
    scrollPercentage: 50 // %
  }
};
</script>
```

### Dashboard Kullanımı

1. **Giriş yapın**: http://localhost:3000
2. **Agent durumunuzu ayarlayın**: Çevrimiçi, Meşgul, Dışarıda, Molada, Rahatsız Etmeyin
3. **Gelen mesajları görüntüleyin**: Sol panelden conversations listesi
4. **Sesli arama kabul edin**: Bildirim geldiğinde Accept butonuna tıklayın
5. **Ticket yönetimi**: Kanban board'dan ticket'ları yönetin
6. **Analytics**: Dashboard'dan detaylı istatistikleri görüntüleyin
7. **Hazır yanıtları kullanın**: `/` yazarak canned responses'ları görün

---

## 🧠 RAG Nasıl Çalışır?

AsistTR, **Retrieval-Augmented Generation (RAG)** teknolojisi kullanarak AI destekli yanıtlar üretir.

### Hibrit Arama Stratejisi

1. **Bilgi Tabanı Oluşturma**: FAQ'ler, dökümanlar sisteme yüklenir
2. **Vektörleştirme**: Metinler embedding'lere dönüştürülür (nomic-embed-text, 768 boyut)
3. **Saklama**: PostgreSQL pgvector eklentisi ile HNSW index kullanılır
4. **Hibrit Sorgulama**: 
   - Text-based arama: Anahtar kelime eşleşmesi (70% ağırlık)
   - Vector-based arama: Semantik benzerlik (30% ağırlık)
5. **Context Oluşturma**: En alakalı paragraflar seçilir (1500 karakter)
6. **Yanıt Üretimi**: Ollama llama3.1:8b, streaming olarak markdown cevap üretir

### Örnek Akış

```
Kullanıcı: "İade süresi kaç gün?"
    ↓
Embedding Oluştur (nomic-embed-text)
    ↓
Hibrit Arama:
  - Text: "iade süresi" keyword match
  - Vector: Cosine similarity search
    ↓
Bulunan: "İade süresi 14 gündür. Kargo ücretsizdir."
    ↓
LLM Prompt (llama3.1:8b):
  "Aşağıdaki metinde yanıt var. Metni AYNEN kullan ve MARKDOWN formatında yaz.
   METİN: [bulunan bilgi]
   Soru: İade süresi kaç gün?"
    ↓
AI Yanıtı (Streaming + Markdown):
  "## İade Süresi
   
   İade süremiz **14 gün**dür. 
   
   - Kargo ücreti **ücretsiz**dir
   - Fatura ile iade edilmelidir"
```

---

## 🛡️ Güvenlik

- ✅ JWT tabanlı kimlik doğrulama
- ✅ Password hashing (bcrypt, 10 rounds)
- ✅ Rate limiting (100 req/15min)
- ✅ Input sanitization
- ✅ XSS & CSRF koruması
- ✅ HTTPS/WSS zorunlu (production)
- ✅ KVKK uyumlu veri saklama (Türkiye)
- ✅ Role-based access control (Admin/Agent)
- ✅ SQL injection koruması (parameterized queries)
- ✅ CORS policy (whitelisted domains)
- ✅ API Key authentication
- ✅ Session management

---

## 📊 Veritabanı Şeması

### Ana Tablolar (30+)

#### `users`
Admin/Agent kullanıcılar
- `id`, `name`, `email`, `password`, `role` (admin/agent/superadmin)
- `site_id`, `department_id`, `skills` (TEXT[])
- `max_chats`, `current_chats`, `priority_level`
- `created_at`, `updated_at`

#### `sites`
Kayıtlı web siteleri
- `id`, `name`, `domain`, `api_key` (unique)
- `created_at`, `updated_at`

#### `visitors`
Ziyaretçiler
- `id`, `site_id`, `session_id`, `name`, `email`
- `ip_address`, `user_agent`, `meta` (JSON)
- `is_vip`, `language`
- `created_at`, `last_seen`

#### `conversations`
Sohbet oturumları
- `id`, `site_id`, `visitor_id`, `agent_id`
- `status` (open/closed), `rating`, `closed_at`
- `created_at`, `updated_at`

#### `messages`
Mesajlar
- `id`, `conversation_id`, `sender_type` (visitor/agent/bot)
- `sender_id`, `body`, `attachments` (JSON)
- `is_read`, `created_at`

#### `tickets`
Ticket'lar
- `id`, `site_id`, `ticket_number`, `visitor_id`, `agent_id`
- `subject`, `message`, `status`, `priority`, `category_id`
- `department_id`, `custom_fields` (JSON)
- `created_at`, `updated_at`

#### `knowledge_base`
RAG bilgi tabanı
- `id`, `site_id`, `title`, `content`
- `embedding` (vector(768)), `tags`
- `created_at`, `updated_at`

#### `dynamic_forms`
Dinamik formlar
- `id`, `site_id`, `name`, `form_config` (JSON)
- `created_at`, `updated_at`

#### `agents_presence`
Agent çevrimiçi durumu
- `agent_id`, `socket_id`
- `status` (online/offline), `state` (Çevrimiçi, Meşgul, Dışarıda, Molada, Rahatsız Etmeyin)
- `state_message`, `state_until`
- `last_seen`

#### `departments`
Departmanlar
- `id`, `site_id`, `name`, `description`
- `created_at`, `updated_at`

#### `voice_calls`
Sesli aramalar
- `id`, `conversation_id`, `visitor_id`, `agent_id`
- `status` (pending/ringing/active/completed/missed/rejected)
- `started_at`, `answered_at`, `ended_at`, `duration`

#### `call_queue`
Arama kuyruğu
- `id`, `conversation_id`, `visitor_id`, `site_id`
- `status` (waiting/assigned/timeout/cancelled)
- `priority`, `queue_position`, `entered_at`

#### `chat_queue`
Sohbet kuyruğu
- `id`, `conversation_id`, `visitor_id`, `site_id`
- `status`, `priority`, `queue_position`, `entered_at`

#### `canned_responses`
Hazır yanıtlar
- `id`, `site_id`, `agent_id`, `title`, `content`
- `shortcut`, `created_at`

#### `notification_preferences`
Bildirim tercihleri
- `user_id`, `new_message`, `new_conversation`, `voice_call`
- `desktop_notifications`, `sound_enabled`

#### `agent_call_availability`
Agent sesli arama durumu
- `agent_id`, `is_available`
- `updated_at`

### Index'ler

```sql
-- Vector similarity search (HNSW)
CREATE INDEX knowledge_base_embedding_idx 
ON knowledge_base 
USING hnsw (embedding vector_cosine_ops) 
WITH (m = 16, ef_construction = 64);

-- Performance indexes
CREATE INDEX idx_conversations_site_status ON conversations(site_id, status);
CREATE INDEX idx_messages_conversation ON messages(conversation_id, created_at);
CREATE INDEX idx_visitors_session ON visitors(site_id, session_id);
CREATE INDEX idx_tickets_status ON tickets(site_id, status);
CREATE INDEX idx_tickets_priority ON tickets(priority);
```

---

## 📚 Dokümantasyon

Detaylı dokümantasyon için `docs/` klasörüne bakın:

- **[ARCHITECTURE.md](docs/ARCHITECTURE.md)** - Sistem mimarisi
- **[API.md](docs/API.md)** - REST API dokümantasyonu
- **[KURULUM.md](docs/KURULUM.md)** - Detaylı kurulum rehberi
- **[FAQ.md](docs/FAQ.md)** - Sık sorulan sorular

Ayrıca:
- **[SISTEM_ANALIZ_RAPORU.md](SISTEM_ANALIZ_RAPORU.md)** - Kapsamlı sistem analizi
- **[SECURITY.md](SECURITY.md)** - Güvenlik dokümantasyonu

---

## 🧪 Test

```bash
# Backend testleri
cd backend
npm test

# Test coverage
npm run test -- --coverage
```

---

## 🐛 Sorun Giderme

### Ollama Modeli Yüklenmiyor

```bash
# Ollama container loglarını kontrol et
docker logs -f asistr_ollama

# Ollama'yı yeniden başlat
docker-compose restart ollama

# Modeli manuel yükle
docker exec -it asistr_ollama ollama pull llama3.1:8b
```

### Veritabanı Bağlantı Hatası

```bash
# PostgreSQL container'ını kontrol et
docker ps | grep postgres

# PostgreSQL loglarını kontrol et
docker logs asistr_postgres

# Veritabanını yeniden başlat
docker-compose restart postgres
```

### Widget Yüklenmiyor

1. API Key'in doğru olduğundan emin olun
2. Browser console'da hataları kontrol edin
3. CORS ayarlarını kontrol edin
4. WebSocket bağlantısını kontrol edin

---

## 🤝 Katkıda Bulunma

Bu proje şu anda **proprietary license** altındadır. Katkıda bulunmak için lütfen iletişime geçin.

---

## 📄 Lisans ve Telif Hakkı

### ⚠️ ÖNEMLİ: Proprietary License

Bu proje **proprietary (tüm hakları saklı)** bir lisans altındadır.

**Copyright (c) 2025 Nurullah Şahin. All rights reserved.**

### 🔒 Kullanım Kısıtlamaları

Bu yazılımı kullanmak, kopyalamak, dağıtmak veya değiştirmek için **açık yazılı izin** gereklidir.

**Yasaklanan Kullanımlar:**
- ❌ Ticari kullanım (izin olmadan)
- ❌ Kodu kopyalama veya dağıtma
- ❌ Kodu değiştirme veya türev eser oluşturma
- ❌ Reverse engineering
- ❌ Rekabet eden ürün veya hizmet geliştirme

**İzin Verilen Kullanımlar:**
- ✅ Akademik araştırma ve eğitim (uygun atıf ile)
- ✅ Kişisel öğrenme ve deneme
- ✅ Yazılı izin ile ticari kullanım

### 📧 Lisans Talebi

Ticari kullanım veya özel lisans için lütfen iletişime geçin:
- **Email**: nurullahsahin0088@gmail.com
- **Konu**: AsistTR License Request

### 📋 Alternatif Lisanslar

- **AGPL-3.0**: Açık kaynak kullanım için `LICENSE.AGPL-3.0` dosyasına bakın
- **Commercial License**: Ticari kullanım için özel lisans anlaşması gerekir

Detaylar için `LICENSE` dosyasına bakın.

---

## 👨‍💻 Geliştirici

**Nurullah Şahin**

- 📧 Email: nurullahsahin0088@gmail.com
- 🐙 GitHub: [@nurullahsahinn](https://github.com/nurullahsahinn)

---

## 📊 Proje İstatistikleri

- **Toplam Kod Satırı**: ~20,000+ LOC
- **Geliştirme Süresi**: 6+ ay
- **Servis Sayısı**: 6 (Backend, Dashboard, Widget, PostgreSQL, Redis, Ollama)
- **API Endpoint**: 50+
- **WebSocket Event**: 30+
- **Database Tablo**: 30+
- **React Component**: 50+
- **Production Ready**: %90 ✅

---

## 🎯 Gelecek Özellikler

- 📱 **Mobil Uygulama**: iOS & Android native app
- 🎨 **Widget Theme Builder**: Dashboard'dan görsel özelleştirme
- 🌍 **Multi-Language UI**: İngilizce, Almanca, Fransızca dil desteği
- 📞 **PSTN Integration**: Telefon sistemi entegrasyonu
- 🔒 **2FA**: İki faktörlü kimlik doğrulama (TOTP)
- 📝 **Chat Transcripts**: PDF/Email export
- 🧪 **A/B Testing**: Widget varyantları karşılaştırma
- 📊 **Advanced Analytics**: Daha detaylı raporlama ve grafikler
- 🤖 **AI Training**: Kendi verilerinizle AI eğitme
- 🔄 **Webhook Support**: Entegrasyonlar için webhook desteği

---

## 🙏 Teşekkürler

Bu proje, açık kaynak topluluğunun katkılarıyla geliştirilmiştir. Kullanılan teknolojiler:

- [Node.js](https://nodejs.org/)
- [React](https://reactjs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Socket.IO](https://socket.io/)
- [Ollama](https://ollama.ai/)
- [LangChain](https://www.langchain.com/)
- [pgvector](https://github.com/pgvector/pgvector)
- [Tailwind CSS](https://tailwindcss.com/)

---

**⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın!**

---

<div align="center">

**Made with ❤️ in Türkiye**

[⬆ Başa Dön](#-asisttr---yerli-ve-milli-canlı-destek-platformu)

</div>
