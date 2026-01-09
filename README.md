# 🇹🇷 AsistTR - Kurumsal Canlı Destek Platformu

<div align="center">

**AI destekli, self-hosted, production-ready kurumsal iletişim ve destek platformu**

[![Docker](https://img.shields.io/badge/Docker-Production%20Ready-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![WebRTC](https://img.shields.io/badge/WebRTC-P2P%20Ready-333333?logo=webrtc)](https://webrtc.org/)
[![Redis](https://img.shields.io/badge/Redis-7-DC382D?logo=redis&logoColor=white)](https://redis.io/)
[![Security](https://img.shields.io/badge/Security-Hardened-success)](https://github.com/)

[Dokümantasyon](#-dokümantasyon) · [Özellikler](#-temel-özellikler) · [Kurulum](#-hızlı-kurulum-docker) · [Mimari](#-mimari-ve-teknoloji-stack)

</div>

---

## 📖 İçindekiler

- [Proje Hakkında](#-proje-hakkında)
- [Temel Özellikler](#-temel-özellikler)
- [Detaylı Özellikler](#-detaylı-özellikler)
- [Mimari ve Teknoloji Stack](#-mimari-ve-teknoloji-stack)
- [Hızlı Kurulum](#-hızlı-kurulum-docker)
- [Yapılandırma](#-yapılandırma)
- [Güvenlik](#-güvenlik)
- [Veritabanı Şeması](#-veritabanı-şeması)
- [API Dokümantasyonu](#-api-dokümantasyonu)
- [Deployment](#-deployment-production)
- [Katkıda Bulunma](#-katkıda-bulunma)
- [Lisans](#-lisans)

---

## 🎯 Proje Hakkında

**AsistTR**, üniversiteler, şirketler ve kurumlar için geliştirilmiş **tamamen Türkçe**, **self-hosted** ve **production-ready** bir müşteri iletişim platformudur.

### 🏆 Neden AsistTR?

- ✅ **%100 Self-Hosted** - Verileriniz sizde kalır (KVKK uyumlu)
- ✅ **Kurumsal Seviye Güvenlik** - Rate limiting, encryption, audit logs
- ✅ **AI Destekli** - Ollama ile tamamen offline çalışan yapay zeka
- ✅ **Multi-Tenant** - Tek platformda sınırsız site yönetimi
- ✅ **Ölçeklenebilir** - Redis adapter ile horizontal scaling
- ✅ **Sıfır Bağımlılık** - Hiçbir SaaS servisine gerek yok
- ✅ **Production-Ready** - Docker, logging, monitoring entegre

### 🎯 Kullanım Senaryoları

| Sektör | Kullanım |
|--------|----------|
| 🎓 **Üniversiteler** | Öğrenci danışmanlığı, kayıt desteği, uzaktan eğitim |
| 🏢 **Şirketler** | Müşteri desteği, satış ekibi iletişimi, teknik destek |
| 🏥 **Hastaneler** | Randevu yönetimi, hasta bilgilendirme |
| 🏛️ **Belediyeler** | Vatandaş hizmetleri, şikayet yönetimi |
| 🛒 **E-Ticaret** | Canlı alışveriş desteği, sipariş takibi |

---

## ⭐ Temel Özellikler

### 💬 **Gerçek Zamanlı İletişim**
- **Canlı Mesajlaşma** - WebSocket ile anlık, kesintisiz iletişim
- **Sesli Arama** - WebRTC P2P ile kristal netliğinde ses kalitesi
- **Görüntülü Konuşma** - HD kalitede (720p), düşük bant genişliği
- **Ekran Paylaşımı** - Sorunları görsel olarak çözme
- **Dosya Paylaşımı** - Resim, PDF, döküman gönderimi (10MB limit)
- **Typing Indicators** - Karşı tarafın yazma durumunu gösterme

### 🤖 **Yapay Zeka (RAG Sistemi)**
- **Esnek LLM Desteği** - Ollama (yerel/offline) veya API (OpenAI, Claude, Gemini)
- **Düşük Donanım Uyumlu** - Gemma 2B (2GB RAM) ile çalışabilir
- **Hibrit Arama** - Vector (pgvector HNSW) + Text-based arama
- **Streaming Yanıtlar** - ChatGPT benzeri karakter karakter görüntüleme
- **Markdown Desteği** - Başlıklar, listeler, kod blokları
- **Context-Aware** - Konuşma geçmişini anlayan akıllı cevaplar
- **Agent Kontrol** - AI'ı durdurma/devam ettirme yetkisi

### 🎫 **Ticket Yönetimi**
- **Kanban Board** - Görsel ticket yönetimi (Yeni → Çözüldü → Kapatıldı)
- **SLA Yönetimi** - İş saatlerine göre akıllı süre hesaplama
- **Ticket Kilitleme** - Aynı anda düzenlemeyi engelleme
- **Şablonlar** - Hazır ticket şablonları ile hızlı yanıt
- **Email Entegrasyonu** - IMAP/SMTP ile otomatik ticket oluşturma
- **Öncelik Seviyeleri** - Düşük, Normal, Yüksek, Acil
- **Özel Alanlar** - Dinamik form alanları

### 👥 **Agent ve Yetkilendirme**
- **Rol Tabanlı Erişim** - SuperAdmin, Admin, Agent
- **Site Bazlı İzolasyon** - Multi-tenant güvenlik
- **Agent Durumları** - Müsait, Uzakta, Meşgul, Molada, Rahatsız Etmeyin
- **Departman Yönetimi** - Ekip organizasyonu
- **Skill-Based Routing** - Yeteneklere göre yönlendirme
- **Performans Metrikleri** - İlk yanıt, ortalama çözüm süresi

### 📊 **Analytics ve Raporlama**
- **Canlı Ziyaretçi İzleme** - Tawk.to benzeri gerçek zamanlı takip
- **Session History** - Detaylı ziyaretçi gezinti geçmişi
- **Activity Analysis** - Aktif/İdle durum takibi, süre analizi
- **Funnel Analysis** - Giriş/çıkış sayfaları, conversion takibi
- **Agent Performance** - İlk yanıt süresi, çözüm oranı
- **CSAT & Rating** - Müşteri memnuniyeti puanlama
- **Audit Logs** - "Kim ne yaptı?" tam denetim izi

### 🛡️ **Güvenlik**
- **Rate Limiting** - DDoS koruması (express-rate-limit)
- **Helmet Security** - XSS, Clickjacking koruması
- **JWT Authentication** - Güvenli oturum yönetimi
- **Redis Encryption** - Şifreli cache
- **SQL Injection Protection** - Parametreli sorgular
- **CORS Policy** - Whitelist domain kontrolü
- **Input Sanitization** - Veri temizleme
- **Audit Trail** - Tüm kritik işlemler loglanır

---

## 🚀 Detaylı Özellikler

### 💬 Mesajlaşma ve İletişim

#### Gerçek Zamanlı Mesajlaşma
- **Socket.IO** ile kesintisiz bağlantı
- **Otomatik yeniden bağlanma** (60sn grace period)
- **Message delivery status** (Gönderildi, İletildi, Okundu)
- **Grup görünümü** - Aynı ziyaretçinin tüm sohbetleri tek başlık altında
- **Session continuity** - Dönüş ziyaretçileri tanıma
- **Mesaj düzenleme/silme** (5 dakika içinde)
- **Dahili notlar** - Agent'lar arası gizli notlar
- **Chat transfer** - Sohbeti başka agent'a devretme
- **Etiketleme** - Kategorilere ayırma ve filtreleme
- **Arama** - Tüm konuşmalarda full-text search

#### Sesli Arama (WebRTC)
```
Özellikler:
✅ P2P bağlantı (düşük latency)
✅ Echo cancellation (yankı önleme)
✅ Noise suppression (gürültü bastırma)
✅ Auto gain control (ses dengeleme)
✅ Mute/Unmute senkronizasyonu
✅ Bağlantı kopunca otomatik cleanup
✅ Call queue - Kuyruk sistemi
✅ Agent availability control
```

#### Görüntülü Konuşma
```
Özellikler:
✅ 720p HD kalite (bandwidth optimizasyonu)
✅ 30 FPS (smooth görüntü)
✅ Ayna efekti (local video için)
✅ Kamera açma/kapama senkronizasyonu
✅ Avatar gösterimi (kamera kapalıyken)
✅ Bağlantı kopunca cleanup
```

#### Ekran Paylaşımı
```
Özellikler:
✅ Track replacement (bağlantı kopmadan geçiş)
✅ Sonsuz ayna önleme
✅ Tarayıcı "Durdur" butonu desteği
✅ Otomatik kameraya geri dönüş
✅ Çizim araçları (koordinat düzeltme v3)
```

---

### 🤖 AI ve RAG Sistemi

#### LLM Seçenekleri ve Konfigürasyon

AsistTR, **esneklik** önceliğiyle tasarlanmıştır. İhtiyacınıza göre yerel veya bulut tabanlı AI kullanabilirsiniz:

##### Seçenek 1: Ollama (Yerel/Offline) ⭐ Önerilen
```yaml
Avantajlar:
  ✅ Tamamen offline çalışır
  ✅ Veri gizliliği (KVKK uyumlu)
  ✅ Sınırsız kullanım (ücretsiz)
  ✅ Düşük latency (yerel)
  
Dezavantajlar:
  ❌ Donanım gereksinimi
  ❌ Model kalitesi (API'lere göre düşük)

Desteklenen Modeller:
  • llama3.1:8b (Önerilen - 5GB RAM, ~4.7GB)
  • llama3.1:70b (Yüksek kalite - 40GB+ RAM)
  • mistral:7b (Hızlı - 4GB RAM, ~4.1GB)
  • gemma:2b (Düşük donanım - 2GB RAM, ~1.4GB) 🔥
  • phi3:mini (Ultra düşük - 2GB RAM, ~2.2GB)
  • qwen2:7b (Çince desteği - 5GB RAM)
```

**Düşük Donanımlı Bilgisayarlar İçin:**
```bash
# Gemma 2B - En hafif model (2GB RAM yeterli)
docker exec -it asistr_ollama ollama pull gemma:2b

# .env dosyasında model değiştir
OLLAMA_MODEL=gemma:2b
```

##### Seçenek 2: OpenAI API (GPT-4, GPT-3.5)
```yaml
Avantajlar:
  ✅ Yüksek kalite
  ✅ Donanım gerektirmez
  ✅ Hızlı güncelleme
  
Dezavantajlar:
  ❌ Ücretli (token bazlı)
  ❌ İnternet gerekli
  ❌ Veri 3. taraf sunucuya gider

Konfigürasyon (.env):
  AI_PROVIDER=openai
  OPENAI_API_KEY=sk-...
  OPENAI_MODEL=gpt-4-turbo
  OPENAI_MAX_TOKENS=500
```

##### Seçenek 3: Anthropic Claude API
```yaml
Avantajlar:
  ✅ Uzun context (100K+ token)
  ✅ Yüksek kalite
  ✅ Markdown desteği mükemmel
  
Konfigürasyon (.env):
  AI_PROVIDER=anthropic
  ANTHROPIC_API_KEY=sk-ant-...
  ANTHROPIC_MODEL=claude-3-sonnet
```

##### Seçenek 4: Google Gemini API
```yaml
Avantajlar:
  ✅ Ücretsiz tier (1M token/gün)
  ✅ Hızlı
  ✅ Multimodal (resim okuma)
  
Konfigürasyon (.env):
  AI_PROVIDER=google
  GOOGLE_API_KEY=AIza...
  GOOGLE_MODEL=gemini-pro
```

##### Seçenek 5: Azure OpenAI
```yaml
Kurumsal için:
  ✅ SLA garantisi
  ✅ Avrupa veri merkezi
  ✅ Compliance (ISO, SOC2)
  
Konfigürasyon (.env):
  AI_PROVIDER=azure
  AZURE_OPENAI_ENDPOINT=https://....openai.azure.com/
  AZURE_OPENAI_KEY=...
  AZURE_DEPLOYMENT_NAME=gpt-4
```

#### Model Karşılaştırması

| Model | RAM | Disk | Kalite | Hız | Maliyet | Önerilen Kullanım |
|-------|-----|------|--------|-----|---------|-------------------|
| **Ollama - Gemma 2B** | 2GB | 1.4GB | ⭐⭐⭐ | ⚡⚡⚡ | Ücretsiz | Düşük donanım |
| **Ollama - Llama 3.1:8B** | 5GB | 4.7GB | ⭐⭐⭐⭐ | ⚡⚡ | Ücretsiz | Dengeli |
| **Ollama - Llama 3.1:70B** | 40GB | 39GB | ⭐⭐⭐⭐⭐ | ⚡ | Ücretsiz | Yüksek kalite |
| **OpenAI GPT-3.5** | 0 | 0 | ⭐⭐⭐⭐ | ⚡⚡⚡ | $0.0005/1K | Hızlı yanıt |
| **OpenAI GPT-4** | 0 | 0 | ⭐⭐⭐⭐⭐ | ⚡⚡ | $0.03/1K | En iyi kalite |
| **Claude 3 Sonnet** | 0 | 0 | ⭐⭐⭐⭐⭐ | ⚡⚡ | $0.003/1K | Uzun metin |
| **Google Gemini Pro** | 0 | 0 | ⭐⭐⭐⭐ | ⚡⚡⚡ | Ücretsiz* | Başlangıç |

*Gemini: Günlük 1M token ücretsiz

#### Backend Konfigürasyon Örneği

**`backend/.env`:**
```env
# AI Provider Seçimi
# Değerler: 'ollama', 'openai', 'anthropic', 'google', 'azure'
AI_PROVIDER=ollama

# === OLLAMA (Yerel/Offline) ===
OLLAMA_URL=http://ollama:11434
OLLAMA_MODEL=llama3.1:8b
# Düşük donanım için: gemma:2b veya phi3:mini

# === OPENAI (API) ===
OPENAI_API_KEY=sk-proj-...
OPENAI_MODEL=gpt-4-turbo
OPENAI_MAX_TOKENS=500
OPENAI_TEMPERATURE=0.7

# === ANTHROPIC CLAUDE (API) ===
ANTHROPIC_API_KEY=sk-ant-api03-...
ANTHROPIC_MODEL=claude-3-sonnet-20240229
ANTHROPIC_MAX_TOKENS=1000

# === GOOGLE GEMINI (API) ===
GOOGLE_API_KEY=AIzaSy...
GOOGLE_MODEL=gemini-pro

# === AZURE OPENAI (Enterprise) ===
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_KEY=...
AZURE_DEPLOYMENT_NAME=gpt-4
AZURE_API_VERSION=2024-02-01

# === Embeddings (Her zaman Ollama kullanılır) ===
EMBEDDING_MODEL=nomic-embed-text
# Bu model hafif olduğu için hep yerel çalışır (768 boyut)
```

#### Provider Implementation (Backend)

```javascript
// backend/src/services/ai.provider.js

class AIProvider {
  static async generate(prompt, options = {}) {
    const provider = process.env.AI_PROVIDER || 'ollama';
    
    switch (provider) {
      case 'ollama':
        return await this.generateOllama(prompt, options);
      case 'openai':
        return await this.generateOpenAI(prompt, options);
      case 'anthropic':
        return await this.generateClaude(prompt, options);
      case 'google':
        return await this.generateGemini(prompt, options);
      case 'azure':
        return await this.generateAzure(prompt, options);
      default:
        throw new Error(`Unknown AI provider: ${provider}`);
    }
  }
  
  // Ollama (Yerel)
  static async generateOllama(prompt, options) {
    const response = await fetch(`${process.env.OLLAMA_URL}/api/generate`, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        model: process.env.OLLAMA_MODEL,
        prompt,
        stream: options.stream || false
      })
    });
    return response;
  }
  
  // OpenAI API
  static async generateOpenAI(prompt, options) {
    const { Configuration, OpenAIApi } = require('openai');
    const configuration = new Configuration({
      apiKey: process.env.OPENAI_API_KEY
    });
    const openai = new OpenAIApi(configuration);
    
    const response = await openai.createChatCompletion({
      model: process.env.OPENAI_MODEL,
      messages: [{ role: 'user', content: prompt }],
      max_tokens: parseInt(process.env.OPENAI_MAX_TOKENS),
      temperature: parseFloat(process.env.OPENAI_TEMPERATURE),
      stream: options.stream || false
    });
    
    return response.data;
  }
  
  // Anthropic Claude
  static async generateClaude(prompt, options) {
    const response = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'x-api-key': process.env.ANTHROPIC_API_KEY,
        'anthropic-version': '2023-06-01'
      },
      body: JSON.stringify({
        model: process.env.ANTHROPIC_MODEL,
        messages: [{ role: 'user', content: prompt }],
        max_tokens: parseInt(process.env.ANTHROPIC_MAX_TOKENS),
        stream: options.stream || false
      })
    });
    return response;
  }
  
  // Google Gemini
  static async generateGemini(prompt, options) {
    const response = await fetch(
      `https://generativelanguage.googleapis.com/v1/models/${process.env.GOOGLE_MODEL}:generateContent?key=${process.env.GOOGLE_API_KEY}`,
      {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          contents: [{ parts: [{ text: prompt }] }]
        })
      }
    );
    return response;
  }
}

module.exports = AIProvider;
```

#### Hibrit Kullanım (En İyi Uygulama)

```javascript
// Hem yerel hem API kullanımı
// Basit sorular için Ollama, karmaşık sorular için OpenAI

async function smartRouting(query, context) {
  const complexity = analyzeComplexity(query);
  
  if (complexity < 5) {
    // Basit soru → Ollama (ücretsiz)
    return await AIProvider.generate(query, { provider: 'ollama' });
  } else {
    // Karmaşık soru → OpenAI (ücretli ama kaliteli)
    return await AIProvider.generate(query, { provider: 'openai' });
  }
}

function analyzeComplexity(query) {
  let score = 0;
  
  // Uzun sorular karmaşıktır
  if (query.length > 200) score += 3;
  
  // Çoklu sorular
  if (query.includes('?') && query.split('?').length > 2) score += 2;
  
  // Teknik terimler
  const technicalTerms = ['API', 'konfigürasyon', 'entegrasyon', 'algoritma'];
  if (technicalTerms.some(term => query.includes(term))) score += 4;
  
  return score;
}
```

#### Maliyet Optimizasyonu

```javascript
// Token kullanımını izle ve bütçeyi kontrol et
const DAILY_BUDGET = 10; // $10/gün
let todaySpent = 0;

async function generateWithBudget(prompt) {
  if (todaySpent >= DAILY_BUDGET) {
    // Bütçe doldu → Ollama'ya geç
    console.warn('Daily budget reached, switching to Ollama');
    return await AIProvider.generate(prompt, { provider: 'ollama' });
  }
  
  const response = await AIProvider.generate(prompt, { provider: 'openai' });
  
  // Maliyeti hesapla
  const cost = (response.usage.total_tokens / 1000) * 0.03; // GPT-4
  todaySpent += cost;
  
  // Veritabanına kaydet
  await query(`
    INSERT INTO ai_usage (date, provider, tokens, cost)
    VALUES (CURRENT_DATE, 'openai', $1, $2)
  `, [response.usage.total_tokens, cost]);
  
  return response;
}
```

---

#### Hibrit Arama Stratejisi
```
1. Bilgi Tabanı Oluşturma
   ↓
2. Embedding (nomic-embed-text, 768 boyut)
   ↓
3. pgvector + HNSW Index
   ↓
4. Hibrit Sorgulama:
   - Text Match: 70% ağırlık
   - Vector Search: 30% ağırlık
   ↓
5. Context (1500 karakter)
   ↓
6. LLM (llama3.1:8b) Streaming Yanıt
```

#### Akış Örneği
```javascript
// Kullanıcı sorusu
"İade süresi kaç gün?"

// 1. Embedding oluştur
const embedding = await embedText(query);

// 2. Hibrit arama
const textResults = await searchByKeyword("iade süresi");
const vectorResults = await searchByVector(embedding);

// 3. Skorlama ve birleştirme
const hybridResults = combine(textResults * 0.7, vectorResults * 0.3);

// 4. Context oluştur
const context = topResults.map(r => r.content).join('\n');

// 5. LLM'e gönder (streaming)
const stream = await ollama.generate({
  model: 'llama3.1:8b',
  prompt: `Aşağıdaki bilgiyi kullanarak yanıt ver:\n${context}\n\nSoru: ${query}`,
  stream: true
});

// 6. Frontend'e karakter karakter gönder
for await (const chunk of stream) {
  socket.emit('ai:chunk', chunk);
}
```

#### Bilgi Tabanı Widget Entegrasyonu
```javascript
// Ziyaretçi "iade" yazınca widget içinde makale öneri
socket.on('message:new', async (data) => {
  const suggestions = await kb.search(data.message, data.siteId);
  
  if (suggestions.length > 0) {
    socket.emit('kb:suggestions', {
      articles: suggestions.slice(0, 3),
      message: "Bu makaleler yardımcı olabilir:"
    });
  }
});
```

---

### 🎫 Ticket Yönetimi

#### SLA (Service Level Agreement)
```javascript
// İş saati hesaplama örneği
// Cuma 17:55'te açılan "1 saat SLA" ticket
// Mesai: 09:00-18:00, Hafta içi

Input:  Cuma 17:55 + 1 saat SLA
Output: Pazartesi 09:55 (hafta sonu ve mesai dışı atlanır)

function addBusinessHours(startDate, hours) {
  while (hoursRemaining > 0) {
    // Hafta sonu kontrolü
    if (isWeekend(date)) {
      date = nextMonday(date);
      continue;
    }
    
    // Mesai dışı kontrolü
    if (date.hour >= 18) {
      date.setDate(date.getDate() + 1);
      date.setHours(9, 0, 0, 0);
      continue;
    }
    
    date.addHours(1);
    hoursRemaining--;
  }
  return date;
}
```

#### Ticket Kilitleme (Conflict Prevention)
```javascript
// Agent ticket açtığında kilit
const lock = await ticketLockService.acquire(ticketId, agentId);

// Başka agent açmaya çalışırsa
if (lock.ownerId !== agentId) {
  return res.status(423).json({
    error: 'Ticket şu anda başka bir agent tarafından düzenleniyor',
    owner: lock.ownerName,
    since: lock.acquiredAt
  });
}

// Agent bağlantı kopunca otomatik serbest bırakma
socket.on('disconnect', async () => {
  await ticketLockService.releaseAllByUser(socket.user.id);
  io.to('agents').emit('ticket:unlocked', { userId: socket.user.id });
});
```

#### Email Entegrasyonu
```yaml
IMAP (Gelen):
  - Gmail, Outlook, özel sunucular
  - Otomatik ticket oluşturma
  - Email -> Ticket dönüşümü
  - Attachment handling

SMTP (Giden):
  - Otomatik bildirimler
  - Email şablonları
  - Ticket güncelleme mailleri
  - HTML + Plain text desteği
```

---

### 👥 Agent Yönetimi ve Yetkilendirme

#### Rol Tabanlı Erişim (RBAC)
```
┌─────────────────┬─────────┬───────┬─────────┐
│ Özellik         │ S.Admin │ Admin │ Agent   │
├─────────────────┼─────────┼───────┼─────────┤
│ Tüm Sitelere    │   ✅    │  ❌   │   ❌    │
│ Site Yönetimi   │   ✅    │  ✅   │   ❌    │
│ Agent Ekleme    │   ✅    │  ✅   │   ❌    │
│ Widget Ayarları │   ✅    │  ✅   │   ❌    │
│ Sohbet          │   ✅    │  ✅   │   ✅    │
│ Ticket Yönetimi │   ✅    │  ✅   │   ✅    │
│ Bilgi Tabanı    │   ✅    │  ✅   │ ✅ (Own)│
│ Hazır Cevaplar  │   ✅    │  ✅   │   ✅    │
│ Analytics       │   ✅    │  ✅   │ ✅ (Own)│
└─────────────────┴─────────┴───────┴─────────┘
```

#### Agent Özellikleri
```javascript
{
  "id": "uuid",
  "name": "Ahmet Yılmaz",
  "email": "ahmet@example.com",
  "role": "agent",
  "site_id": "uuid",
  "department_id": "uuid",
  
  // Yetenekler
  "skills": ["Teknik Destek", "Satış", "İngilizce"],
  
  // Kapasite
  "max_chats": 5,
  "current_chats": 2,
  "priority_level": 1,
  
  // Durum
  "status": "online",
  "state": "Müsait", // Müsait, Meşgul, Molada, Uzakta
  "state_message": "Öğle yemeğinde",
  "state_until": "2026-01-09T14:00:00Z",
  
  // Sesli arama
  "accept_calls": true
}
```

#### Routing Stratejileri
```javascript
const routingStrategies = {
  ROUND_ROBIN: 'Sıralı dağıtım',
  LEAST_BUSY: 'En az meşgul agent',
  SKILL_BASED: 'Yetenek bazlı',
  DEPARTMENT: 'Departman bazlı',
  VIP_PRIORITY: 'VIP öncelikli',
  LANGUAGE: 'Dil bazlı'
};

// Örnek: Skill-based routing
const bestAgent = await findBestAgent({
  requiredSkills: ['Teknik Destek', 'İngilizce'],
  site_id: siteId,
  status: 'online',
  state: ['Müsait', 'Meşgul'],
  max_chats_not_exceeded: true
});
```

---

### 📊 Analytics ve Ziyaretçi Takibi

#### Canlı Ziyaretçi İzleme
```javascript
// Real-time visitor tracking
{
  "visitor_id": "uuid",
  "session_id": "session_xyz",
  "name": "Mehmet A.",
  "email": "mehmet@example.com",
  "ip_address": "185.x.x.x",
  "location": {
    "country": "Turkey",
    "city": "Istanbul",
    "coordinates": [41.0082, 28.9784]
  },
  
  // Tarayıcı bilgileri
  "browser": "Chrome 120",
  "os": "Windows 11",
  "device": "Desktop",
  "screen": "1920x1080",
  
  // Aktivite
  "status": "active", // active, idle, offline
  "current_page": "/products/laptop",
  "page_title": "Laptop Ürünleri",
  "time_on_page": 45, // saniye
  "scroll_depth": 75, // %
  
  // Gezinti geçmişi
  "page_history": [
    {
      "url": "/",
      "title": "Ana Sayfa",
      "duration": 30,
      "timestamp": "2026-01-09T10:00:00Z"
    },
    {
      "url": "/products",
      "title": "Ürünler",
      "duration": 60,
      "timestamp": "2026-01-09T10:00:30Z"
    }
  ],
  
  // Metrikler
  "page_views": 5,
  "total_duration": 180, // saniye
  "visit_count": 3,
  "first_visit": "2026-01-05T10:00:00Z",
  "last_seen": "2026-01-09T10:03:00Z"
}
```

#### Session History (Persistent Data)
```javascript
// visitor_sessions tablosuna kaydedilen veri
{
  "id": "uuid",
  "visitor_id": "uuid",
  "session_id": "session_xyz",
  "site_id": "uuid",
  
  // Toplam metrikler
  "total_duration_seconds": 180,
  "page_views": 5,
  
  // Detaylı aktivite
  "activity_timeline": [
    {
      "timestamp": "2026-01-09T10:00:00Z",
      "action": "page_view",
      "page": "/",
      "duration": 30
    },
    {
      "timestamp": "2026-01-09T10:00:15Z",
      "action": "idle_start"
    },
    {
      "timestamp": "2026-01-09T10:00:45Z",
      "action": "active"
    }
  ],
  
  // Sayfa listesi
  "pages_visited": [
    {
      "url": "/",
      "title": "Ana Sayfa",
      "visits": 2,
      "total_time": 45
    }
  ],
  
  // Oturum bilgisi
  "started_at": "2026-01-09T10:00:00Z",
  "ended_at": "2026-01-09T10:03:00Z"
}
```

#### Agent Performance Metrics
```javascript
{
  "agent_id": "uuid",
  "period": "last_30_days",
  
  // Yanıt süreleri
  "first_response_time": {
    "average": 45, // saniye
    "median": 30,
    "min": 5,
    "max": 180
  },
  
  "average_response_time": {
    "average": 120,
    "median": 90
  },
  
  "resolution_time": {
    "average": 600, // 10 dakika
    "median": 480
  },
  
  // Metrikler
  "total_conversations": 150,
  "resolved_count": 120,
  "resolution_rate": 0.80, // %80
  
  "total_tickets": 50,
  "closed_tickets": 40,
  "closure_rate": 0.80,
  
  // Memnuniyet
  "average_rating": 4.5,
  "rating_distribution": {
    "5": 30,
    "4": 15,
    "3": 3,
    "2": 1,
    "1": 1
  },
  
  // Aktivite
  "online_hours": 160,
  "active_hours": 120,
  "idle_hours": 40
}
```

---

### 🎨 Widget Özelleştirme

#### Widget Senaryoları (İş Saatlerine Göre Akışlar)

AsistTR, **akıllı routing** ile ziyaretçilere her durumda en iyi deneyimi sunar:

##### Senaryo 1: Mesai İçi + Agent Müsait ✅
```
┌─────────────────────────────────────────┐
│ 1. Widget açılır                        │
│    💬 "Merhaba, nasıl yardımcı olabilirim?" │
└─────────────┬───────────────────────────┘
              │
              ↓ Kullanıcı mesaj yazar
┌─────────────────────────────────────────┐
│ 2. Routing Engine Çalışır               │
│    • Agent durumu: Online (Müsait)      │
│    • Kapasite: 2/5 sohbet               │
│    → Agent'a ANINDA atar                │
└─────────────┬───────────────────────────┘
              │
              ↓
┌─────────────────────────────────────────┐
│ 3. İki Paralel Akış:                    │
│                                          │
│ A) AI Cevap Önerisi (Agent'a)           │
│    🤖 AI context'e bakıp öneri üretir   │
│    Agent "Gönder" veya "Düzenle"        │
│                                          │
│ B) Agent Manuel Yanıt                   │
│    👤 Agent direkt yazabilir            │
└─────────────┬───────────────────────────┘
              │
              ↓ Sorun çözüldü
┌─────────────────────────────────────────┐
│ 4. Sohbet Kapatma                       │
│    Agent: "Başka yardım?"               │
│    Kullanıcı: "Hayır teşekkürler"      │
│    → Sohbet kapatılır                   │
│    → Rating: ⭐⭐⭐⭐⭐               │
└─────────────────────────────────────────┘
```

**Kullanıcı Görünümü:**
```
Widget
├─ 💬 Canlı Sohbet
├─ ⏱️  Ortalama yanıt: 45 saniye
├─ 🟢 5 temsilci çevrimiçi
└─ 📞 Sesli arama butonu (aktif)
```

---

##### Senaryo 2: Mesai İçi + Agent YOK (Hepsi Meşgul) 🤖
```
┌─────────────────────────────────────────┐
│ 1. Widget açılır                        │
│    💬 "Merhaba, nasıl yardımcı olabilirim?" │
└─────────────┬───────────────────────────┘
              │
              ↓ Kullanıcı mesaj yazar
┌─────────────────────────────────────────┐
│ 2. Routing Engine Kontrol               │
│    • Tüm agent'lar: Meşgul (5/5)       │
│    • Queue: 3 kişi bekliyor             │
│    → AI devreye girer                   │
└─────────────┬───────────────────────────┘
              │
              ↓
┌─────────────────────────────────────────┐
│ 3. AI Yanıt #1 (Otomatik)               │
│    🤖 RAG: "İade süremiz 14 gündür..."  │
│    Widget: AI rozeti gösterir           │
│    [🤖 AI Asistan yanıtlıyor]           │
└─────────────┬───────────────────────────┘
              │
              ↓ Kullanıcı ek soru sorar
┌─────────────────────────────────────────┐
│ 4. AI Yanıt #2                          │
│    🤖 "Kargo ücretsizdir..."            │
└─────────────┬───────────────────────────┘
              │
              ↓ 3 saniye bekle
┌─────────────────────────────────────────┐
│ 5. Escalation Seçeneği (Otomatik)       │
│    ╔════════════════════════════════╗   │
│    ║ 💡 Bu bilgiler yardımcı olmadıysa: ║
│    ║                                 ║   │
│    ║ [🧑 Temsilci Bekle]            ║   │
│    ║ Sıra: 3, Tahmini: ~2 dakika   ║   │
│    ║                                 ║   │
│    ║ [📧 Ticket Oluştur]            ║   │
│    ║ Email'e yanıt gönderilir       ║   │
│    ╚════════════════════════════════╝   │
└─────────────┬───────────────────────────┘
              │
              ├─→ Temsilci Bekle seçerse:
              │   → Queue'ya eklenir
              │   → Position tracker gösterilir
              │   → Agent müsait olunca bağlanır
              │
              └─→ Ticket Oluştur seçerse:
                  → Form açılır (Ad, Email, Konu)
                  → Ticket otomatik oluşturulur
                  → Email confirmation gönderilir
```

**Kullanıcı Görünümü:**
```
Widget
├─ 🤖 AI Asistan
├─ 💬 "İade süremiz 14 gündür..."
├─ ⏳ Kuyruk: 3 kişi (~2 dk)
└─ 📞 Sesli arama: Devre dışı (meşgul)
```

**Queue Position Tracker:**
```
╔═══════════════════════════════════╗
║  Sıranız: 3 → 2 → 1              ║
║  ⏱️  Tahmini bekleme: 1 dk 30 sn  ║
║  🟡 Tüm temsilciler meşgul        ║
║                                   ║
║  [❌ Kuyruktan Çık]              ║
╚═══════════════════════════════════╝
```

---

##### Senaryo 3: Mesai DIŞI (Gece/Hafta Sonu) 🌙
```
┌─────────────────────────────────────────┐
│ 1. Widget açılır (Otomatik Mesaj)       │
│    ╔═══════════════════════════════╗    │
│    ║ 🌙 Temsilcilerimiz Çevrimdışı ║    │
│    ║                               ║    │
│    ║ Mesai Saatleri:               ║    │
│    ║ 📅 Pazartesi - Cuma           ║    │
│    ║ 🕐 09:00 - 18:00 (GMT+3)     ║    │
│    ║ 🚫 Cumartesi - Pazar Kapalı  ║    │
│    ║                               ║    │
│    ║ Şu an: Pazar, 22:30          ║    │
│    ║ Açılış: Pazartesi 09:00      ║    │
│    ║ (⏱️  10 saat 30 dakika sonra) ║    │
│    ╚═══════════════════════════════╝    │
└─────────────┬───────────────────────────┘
              │
              ↓
┌─────────────────────────────────────────┐
│ 2. Seçenekler Sunulur                   │
│    ╔═══════════════════════════════╗    │
│    ║ Size nasıl yardımcı olabiliriz? ║  │
│    ║                               ║    │
│    ║ [🤖 AI ile Devam Et]         ║    │
│    ║ Anında yanıt alın             ║    │
│    ║                               ║    │
│    ║ [📧 Ticket Oluştur]          ║    │
│    ║ Email ile yanıtlarız          ║    │
│    ╚═══════════════════════════════╝    │
└─────────────┬───────────────────────────┘
              │
              ├─→ AI ile Devam seçerse:
              │   → Normal AI sohbet başlar
              │   → RAG sistemi aktif
              │   → Agent müsait olsa bile atanmaz
              │   → Kayıt edilir (offline_messages)
              │
              └─→ Ticket Oluştur seçerse:
                  → Detaylı form açılır
                  → Department seçimi
                  → Priority seçimi
                  → File upload
                  → Auto-reply: "Pazartesi 09:00'da..."
```

**Kullanıcı Görünümü:**
```
Widget
├─ 🌙 Mesai Dışı Modu
├─ 🕐 Açılış: Pazartesi 09:00
├─ 🤖 AI Asistan (aktif)
├─ 📧 Ticket Oluştur
└─ 📞 Sesli arama: Devre dışı
```

**Ticket Form (Mesai Dışı):**
```
╔═════════════════════════════════════╗
║ 📝 Destek Talebi Oluştur           ║
╠═════════════════════════════════════╣
║ Ad Soyad:    [_________________]    ║
║ Email:       [_________________]    ║
║ Telefon:     [_________________]    ║
║                                     ║
║ Departman:   [▼ Teknik Destek   ]   ║
║ Öncelik:     [▼ Normal          ]   ║
║                                     ║
║ Konu:        [_________________]    ║
║                                     ║
║ Mesaj:       [___________________]  ║
║              [___________________]  ║
║              [___________________]  ║
║                                     ║
║ Dosya Ekle:  [📎 Dosya Seç]        ║
║                                     ║
║ [Gönder]                            ║
╚═════════════════════════════════════╝

✅ Talebiniz alındıktan sonra:
• Ticket #12345 oluşturulur
• Email confirmation gönderilir
• Pazartesi 09:00'da temsilci atanır
• SLA: Normal (8 saat) → Pazartesi 17:00
```

---

#### Durum Geçişleri (State Transitions)

```
Widget Durumları:

1. ONLINE (Mesai İçi + Agent Var)
   ├─ Anında bağlantı
   ├─ Sesli arama aktif
   ├─ Typing indicator aktif
   └─ AI assist (agent'a)

2. BUSY (Mesai İçi + Agent Yok)
   ├─ AI otomatik yanıt
   ├─ Queue sistemi aktif
   ├─ Escalation seçenekleri
   └─ Position tracking

3. OFFLINE (Mesai Dışı)
   ├─ Business hours bilgisi
   ├─ AI sohbet (opsiyonel)
   ├─ Ticket form
   └─ No real-time calls

Geçişler:
• 09:00 → OFFLINE → ONLINE
• Agent sayısı = 0 → ONLINE → BUSY
• 18:00 → ONLINE → OFFLINE
• Queue boşaldı → BUSY → ONLINE
```

---

#### Business Hours Configuration

**Backend (`business_hours` tablosu):**
```sql
-- Hafta içi (Pazartesi-Cuma)
INSERT INTO business_hours (site_id, day_of_week, start_time, end_time)
VALUES 
  ('site-uuid', 1, '09:00', '18:00'), -- Pazartesi
  ('site-uuid', 2, '09:00', '18:00'), -- Salı
  ('site-uuid', 3, '09:00', '18:00'), -- Çarşamba
  ('site-uuid', 4, '09:00', '18:00'), -- Perşembe
  ('site-uuid', 5, '09:00', '18:00'); -- Cuma

-- Hafta sonu (Kapalı)
INSERT INTO business_hours (site_id, day_of_week, is_working_day)
VALUES 
  ('site-uuid', 6, false), -- Cumartesi
  ('site-uuid', 0, false); -- Pazar

-- Tatil günleri
INSERT INTO holidays (site_id, date, name)
VALUES 
  ('site-uuid', '2026-10-29', 'Cumhuriyet Bayramı'),
  ('site-uuid', '2026-04-23', '23 Nisan');
```

**Widget Check (Frontend):**
```javascript
// Widget her açılışta kontrol eder
async function checkBusinessHours() {
  const response = await fetch('/api/settings/business-hours/check', {
    headers: { 'X-Site-ID': siteId }
  });
  
  const { isOpen, nextOpenTime, currentStatus } = await response.json();
  
  if (!isOpen) {
    showOfflineMode(nextOpenTime);
    disableVoiceCall();
    showTicketOption();
  } else {
    // Agent müsaitlik kontrolü
    const agents = await fetch('/api/agents/available');
    if (agents.count === 0) {
      showBusyMode();
      enableQueueOption();
    } else {
      showOnlineMode();
      enableVoiceCall();
    }
  }
}

// Örnek response:
{
  "isOpen": false,
  "currentStatus": "closed",
  "reason": "outside_business_hours",
  "currentTime": "2026-01-09T22:30:00Z",
  "nextOpenTime": "2026-01-10T09:00:00Z",
  "hoursUntilOpen": 10.5,
  "businessHours": {
    "monday": "09:00-18:00",
    "tuesday": "09:00-18:00",
    "wednesday": "09:00-18:00",
    "thursday": "09:00-18:00",
    "friday": "09:00-18:00",
    "saturday": "closed",
    "sunday": "closed"
  }
}
```

---

#### Özel Durumlar

##### Durum 1: Öğle Arası (12:00-13:00)
```
• Tüm agent'lar "Molada"
• Widget: BUSY modu
• AI yanıt verir
• Queue: Aktif (bekleme 13:00'a kadar)
• Mesaj: "🍽️ Öğle arası, 13:00'te döneceğiz"
```

##### Durum 2: Agent Aniden Çıktı (Disconnect)
```
• Sohbet devam ediyor
• Agent bağlantısı koptu
• 60 saniye grace period
• Widget mesajı: "⚠️ Bağlantı sorunu, yeniden bağlanıyor..."
• 60 sn geçtiyse → Başka agent'a transfer
• Transfer başarısızsa → AI devreye girer
```

##### Durum 3: Tatil Günü Özel Mesajı
```
Widget:
╔═══════════════════════════════════╗
║ 🎉 Cumhuriyet Bayramı             ║
║                                   ║
║ 29 Ekim Çarşamba günü kapalıyız  ║
║ 30 Ekim Perşembe 09:00'da        ║
║ hizmetinizdeyiz!                  ║
║                                   ║
║ [🤖 AI Asistan] [📧 Ticket]      ║
╚═══════════════════════════════════╝
```

##### Durum 4: Emergency Override
```javascript
// Admin acil durum açabilir (sistem çökmesi vs)
await setEmergencyMode({
  enabled: true,
  message: "🚨 Teknik bakım: 22:00-23:00\nAcil durumlar: +90 555 123 4567",
  allowAI: false,
  allowTickets: true
});

// Widget tüm sohbetleri kapatır ve mesajı gösterir
```

---

### 🎨 Widget Temel Yapılandırma
```html
<script>
(function(){
  window.AsistTRConfig = {
    // Zorunlu
    apiKey: 'YOUR_API_KEY_HERE',
    
    // Opsiyonel (Varsayılanlar)
    apiUrl: 'https://api.asisttr.com',
    wsUrl: 'wss://api.asisttr.com',
    
    // Görünüm
    primaryColor: '#4F46E5',
    secondaryColor: '#10B981',
    position: 'right', // 'left' or 'right'
    zIndex: 9999,
    
    // Mesajlar
    welcomeMessage: 'Merhaba! Size nasıl yardımcı olabilirim?',
    placeholderText: 'Mesajınızı yazın...',
    agentName: 'Destek Ekibi',
    agentAvatar: 'https://example.com/avatar.png',
    
    // Proactive Chat
    proactiveChat: {
      enabled: true,
      triggers: {
        timeOnPage: 30,        // 30 saniye sonra
        scrollPercentage: 50,  // %50 scroll sonra
        exitIntent: true,      // Çıkış hareketi
        idle: 60,              // 60sn idle sonra
        pageVisibility: true   // Sekmeye dönünce
      },
      message: '👋 Yardıma ihtiyacınız var mı?'
    },
    
    // Özellikler
    features: {
      voiceCall: true,
      videoCall: true,
      fileUpload: true,
      emoticons: true,
      typing: true
    },
    
    // Form
    preChat: {
      enabled: true,
      fields: ['name', 'email', 'phone'],
      required: ['name', 'email']
    },
    
    // Özelleştirme
    customCSS: `
      .asisttr-widget { 
        border-radius: 20px;
      }
      .asisttr-message {
        font-family: 'Inter', sans-serif;
      }
    `,
    
    // Events
    onReady: function() {
      console.log('Widget hazır');
    },
    onOpen: function() {
      console.log('Widget açıldı');
    },
    onMessageSent: function(message) {
      console.log('Mesaj gönderildi:', message);
    },
    onCallStarted: function() {
      console.log('Arama başladı');
    }
  };
  
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = 'https://cdn.asisttr.com/widget.js';
  var x = document.getElementsByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();
</script>
```

#### JavaScript API
```javascript
// Widget kontrolü
AsistTR.open();              // Widget'ı aç
AsistTR.close();             // Widget'ı kapat
AsistTR.toggle();            // Aç/Kapat

// Mesaj gönderme
AsistTR.sendMessage('Merhaba, yardım lazım');

// Bilgi güncelleme
AsistTR.updateVisitor({
  name: 'Ahmet Yılmaz',
  email: 'ahmet@example.com',
  phone: '+905551234567',
  customData: {
    membership: 'Premium',
    lastPurchase: '2026-01-01'
  }
});

// Event dinleme
AsistTR.on('message:received', function(message) {
  console.log('Yeni mesaj:', message);
});

AsistTR.on('call:incoming', function(call) {
  console.log('Gelen arama:', call);
});

// Widget durumu
AsistTR.isOpen();            // true/false
AsistTR.getUnreadCount();    // 3
AsistTR.getVisitorId();      // "uuid"
```

---

## 🔄 Operasyonel Akışlar ve Sistem Mantığı

### 📞 Kuyruk Yönetimi (Queue Management)

#### Sohbet Kuyruğu Akışı
```
1. Ziyaretçi widget'tan "Sohbet Başlat" tıklar
   ↓
2. Sistem müsait agent arar (routing stratejisine göre)
   ↓
3a. Agent VARSA:
   → Direkt bağlan
   → Socket odası oluştur
   → Sohbet başlar
   
3b. Agent YOKSA:
   → Kuyruğa ekle (Redis Queue)
   → Kuyruk pozisyonu hesapla
   → Tahmini bekleme süresi göster
   → Widget'ta "Sıranız: 3, Tahmini: 2 dakika"
   ↓
4. Agent müsait olunca:
   → Kuyruktan ilk kişi çekilir (FIFO/Priority)
   → Socket notification → Agent dashboard
   → Otomatik atama veya manuel kabul
   ↓
5. Bekleme timeout (5 dakika):
   → Otomatik offline mesaj formuna dönüş
   → Veya callback talep formu
```

#### Queue Data Structure (Redis)
```javascript
// Redis Sorted Set kullanımı
ZADD queue:site:{siteId}:visitors {timestamp} {visitorId}

// Queue item structure
{
  "visitor_id": "uuid",
  "session_id": "session_xyz",
  "queue_position": 3,
  "wait_time": 120, // saniye
  "priority": 1, // 1-5 (VIP = 5)
  "department_id": "uuid",
  "required_skills": ["Teknik Destek"],
  "entered_at": "2026-01-09T10:00:00Z",
  "estimated_agent_available": "2026-01-09T10:02:00Z"
}
```

#### Priority Queue Logic
```javascript
// Öncelik hesaplama
function calculatePriority(visitor) {
  let priority = 1; // Base
  
  // VIP müşteri
  if (visitor.is_vip) priority += 4;
  
  // Dönüş müşteri (geçmişte satın almış)
  if (visitor.purchase_history > 0) priority += 2;
  
  // Acil departman (Satış)
  if (visitor.department === 'sales') priority += 1;
  
  // Bekleme süresi (her 2 dakikada +1)
  priority += Math.floor(visitor.wait_time / 120);
  
  return Math.min(priority, 10); // Max 10
}

// Kuyruktan çekme algoritması
async function getNextFromQueue(siteId) {
  // 1. En yüksek priority'li ziyaretçiyi al
  const visitors = await redis.zrevrange(`queue:${siteId}`, 0, -1, 'WITHSCORES');
  
  // 2. Priority hesapla ve sırala
  const sorted = visitors.map(v => ({
    ...v,
    priority: calculatePriority(v)
  })).sort((a, b) => b.priority - a.priority);
  
  // 3. İlk sıradakini döndür
  return sorted[0];
}
```

---

### 🎯 Sohbet Atama Mantığı (Chat Assignment Logic)

#### Routing Stratejileri - Detaylı

##### 1. Round Robin (Sıralı Dağıtım)
```javascript
async function roundRobinAssignment(siteId) {
  // 1. Tüm müsait agent'ları getir
  const agents = await getAvailableAgents(siteId);
  
  // 2. Son atanan agent'ı bul
  const lastAssigned = await redis.get(`round_robin:${siteId}:last`);
  
  // 3. Bir sonrakini seç (circular)
  const currentIndex = agents.findIndex(a => a.id === lastAssigned);
  const nextIndex = (currentIndex + 1) % agents.length;
  const selectedAgent = agents[nextIndex];
  
  // 4. Güncelkaydet
  await redis.set(`round_robin:${siteId}:last`, selectedAgent.id);
  
  return selectedAgent;
}

// Örnek:
// Agent listesi: [A, B, C]
// 1. Sohbet → A
// 2. Sohbet → B
// 3. Sohbet → C
// 4. Sohbet → A (tekrar başa dön)
```

##### 2. Least Busy (En Az Meşgul)
```javascript
async function leastBusyAssignment(siteId) {
  const agents = await getAvailableAgents(siteId);
  
  // Her agent için yük hesapla
  const withLoad = await Promise.all(
    agents.map(async (agent) => ({
      ...agent,
      load: await calculateAgentLoad(agent.id)
    }))
  );
  
  // En düşük yük skoruna sahip agent'ı seç
  const sorted = withLoad.sort((a, b) => a.load - b.load);
  return sorted[0];
}

function calculateAgentLoad(agentId) {
  // Load Skoru = (Aktif Sohbet / Max Sohbet) * 100 + Kuyruk
  const active = agent.current_chats;
  const max = agent.max_chats;
  const queued = agent.queued_chats || 0;
  
  return ((active / max) * 100) + (queued * 10);
}

// Örnek:
// Agent A: 2/5 aktif, 0 kuyruk → Load: 40
// Agent B: 4/5 aktif, 1 kuyruk → Load: 90
// Agent C: 1/5 aktif, 0 kuyruk → Load: 20
// Seçilen: Agent C (en düşük yük)
```

##### 3. Skill-Based (Yetenek Bazlı)
```javascript
async function skillBasedAssignment(siteId, requiredSkills) {
  const agents = await getAvailableAgents(siteId);
  
  // Skill match skoru hesapla
  const scored = agents.map(agent => {
    const matchCount = requiredSkills.filter(skill => 
      agent.skills.includes(skill)
    ).length;
    
    const matchRatio = matchCount / requiredSkills.length;
    const loadScore = calculateAgentLoad(agent.id);
    
    // %70 skill match, %30 load
    const finalScore = (matchRatio * 0.7) + ((100 - loadScore) / 100 * 0.3);
    
    return { agent, score: finalScore };
  });
  
  // En yüksek skoru seç
  const best = scored.sort((a, b) => b.score - a.score)[0];
  return best.agent;
}

// Örnek:
// Ziyaretçi talep: ["İngilizce", "Teknik Destek"]
// Agent A: ["İngilizce", "Teknik Destek", "Satış"] → %100 match
// Agent B: ["Türkçe", "Teknik Destek"] → %50 match
// Agent C: ["İngilizce", "Satış"] → %50 match
// Seçilen: Agent A
```

##### 4. Department Routing (Departman Bazlı)
```javascript
async function departmentRouting(siteId, departmentId) {
  // 1. İlgili departmandaki agent'ları getir
  const agents = await query(`
    SELECT * FROM users 
    WHERE site_id = $1 
      AND department_id = $2
      AND status = 'online'
      AND state IN ('Müsait', 'Meşgul')
      AND current_chats < max_chats
    ORDER BY current_chats ASC
  `, [siteId, departmentId]);
  
  if (agents.length === 0) {
    // Departmanda kimse yoksa genel havuza yönlendir
    return await roundRobinAssignment(siteId);
  }
  
  // En az meşgul agent'ı seç
  return agents[0];
}

// Örnek Departmanlar:
// • Satış → Ürün bilgisi, fiyat teklifi
// • Teknik Destek → Sorun giderme
// • Muhasebe → Fatura, ödeme
```

##### 5. VIP Priority (VIP Öncelikli)
```javascript
async function vipPriorityAssignment(siteId, visitor) {
  if (visitor.is_vip) {
    // VIP için en deneyimli agent'ı seç
    const agents = await query(`
      SELECT u.*, 
             COUNT(c.id) as total_chats,
             AVG(cr.rating) as avg_rating
      FROM users u
      LEFT JOIN conversations c ON c.agent_id = u.id
      LEFT JOIN conversation_ratings cr ON cr.conversation_id = c.id
      WHERE u.site_id = $1 
        AND u.status = 'online'
        AND u.current_chats < u.max_chats
      GROUP BY u.id
      ORDER BY u.priority_level DESC, avg_rating DESC
      LIMIT 1
    `, [siteId]);
    
    return agents[0];
  }
  
  // VIP değilse normal routing
  return await leastBusyAssignment(siteId);
}
```

##### 6. Language-Based (Dil Bazlı)
```javascript
async function languageBasedRouting(siteId, visitorLanguage) {
  const agents = await query(`
    SELECT * FROM users 
    WHERE site_id = $1 
      AND status = 'online'
      AND $2 = ANY(languages)  -- Agent'ın konuştuğu diller
      AND current_chats < max_chats
    ORDER BY current_chats ASC
  `, [siteId, visitorLanguage]);
  
  if (agents.length === 0) {
    // İlgili dilde agent yoksa İngilizce bilen ara
    return await languageBasedRouting(siteId, 'en');
  }
  
  return agents[0];
}

// Örnek:
// Ziyaretçi dili: Almanca
// Agent A: [Türkçe, İngilizce, Almanca] → Seçilir
// Agent B: [Türkçe, İngilizce] → Pas geç
```

---

### 👤 Agent Durumları ve İş Akışı

#### Agent Status Workflow
```
┌─────────────┐
│  Çevrimdışı │ (Offline)
└──────┬──────┘
       │ Login
       ↓
┌─────────────┐
│   Çevrimiçi │ (Online - Müsait)
└──────┬──────┘
       │
       ├─→ Sohbet atandı → "Meşgul" (max_chats'e ulaşana kadar)
       │
       ├─→ Manuel değiştirme → "Uzakta" / "Molada" / "Rahatsız Etmeyin"
       │   (Bu durumlarda yeni sohbet atanmaz ama mevcut sohbetler devam eder)
       │
       ├─→ 60 saniye inaktif → "Çevrimdışı" (grace period)
       │
       └─→ Logout → "Çevrimdışı"
```

#### Agent Capacity Management
```javascript
async function canAcceptNewChat(agentId) {
  const agent = await getAgent(agentId);
  
  // 1. Durumlar kontrolü
  if (agent.status === 'offline') return false;
  if (agent.state === 'Rahatsız Etmeyin') return false;
  if (agent.state === 'Uzakta') return false;
  
  // 2. Kapasite kontrolü
  if (agent.current_chats >= agent.max_chats) return false;
  
  // 3. State süresi kontrolü (geçici durum)
  if (agent.state_until && new Date() < new Date(agent.state_until)) {
    return false; // "Molada - 15:30'a kadar" gibi
  }
  
  return true;
}

// Örnek durum:
{
  "agent_id": "uuid",
  "status": "online",
  "state": "Molada",
  "state_message": "Öğle yemeği",
  "state_until": "2026-01-09T14:00:00Z", // 14:00'a kadar molada
  "current_chats": 2, // Mevcut sohbetler devam ediyor
  "max_chats": 5
}
```

---

### 🎬 Proactive Chat (Otomatik Sohbet Başlatma)

#### Trigger Mekanizmaları

##### 1. Time on Page (Sayfa Süresi)
```javascript
// Widget tracking.js
let pageLoadTime = Date.now();

setInterval(() => {
  const timeOnPage = (Date.now() - pageLoadTime) / 1000;
  
  if (timeOnPage >= AsistTRConfig.proactiveChat.timeOnPage) {
    if (!hasShownProactive) {
      showProactiveMessage();
      hasShownProactive = true;
    }
  }
}, 1000);

// Örnek: 30 saniye sonra
// "👋 Yardıma ihtiyacınız var mı?"
```

##### 2. Scroll Percentage (Kaydırma Yüzdesi)
```javascript
let maxScrollPercentage = 0;

window.addEventListener('scroll', throttle(() => {
  const scrollTop = window.pageYOffset;
  const docHeight = document.documentElement.scrollHeight;
  const winHeight = window.innerHeight;
  
  const scrollPercent = (scrollTop / (docHeight - winHeight)) * 100;
  maxScrollPercentage = Math.max(maxScrollPercentage, scrollPercent);
  
  if (maxScrollPercentage >= AsistTRConfig.proactiveChat.scrollPercentage) {
    if (!hasShownProactive) {
      showProactiveMessage();
      hasShownProactive = true;
    }
  }
}, 500));

// Örnek: %50 scroll sonra
// "İlgilendiğiniz ürün hakkında bilgi verebilirim!"
```

##### 3. Exit Intent (Çıkış Niyeti)
```javascript
document.addEventListener('mouseleave', (e) => {
  if (e.clientY <= 0 && !hasShownProactive) {
    // Mouse ekranın üstüne çıktı (muhtemelen sekmeyi kapatacak)
    showProactiveMessage("Ayrılmadan önce size yardımcı olabilir miyim?");
    hasShownProactive = true;
  }
});
```

##### 4. Idle Detection (Boşta Algılama)
```javascript
let idleTimer;
let lastActivity = Date.now();

function resetIdleTimer() {
  lastActivity = Date.now();
  clearTimeout(idleTimer);
  
  idleTimer = setTimeout(() => {
    const idleTime = (Date.now() - lastActivity) / 1000;
    
    if (idleTime >= AsistTRConfig.proactiveChat.idle && !hasShownProactive) {
      showProactiveMessage("Hala sayfadasınız, yardıma ihtiyacınız var mı?");
      hasShownProactive = true;
    }
  }, AsistTRConfig.proactiveChat.idle * 1000);
}

['mousemove', 'keydown', 'scroll', 'click'].forEach(event => {
  document.addEventListener(event, resetIdleTimer);
});
```

##### 5. Page Visibility (Sekme Değiştirme)
```javascript
document.addEventListener('visibilitychange', () => {
  if (!document.hidden && !hasShownProactive) {
    // Kullanıcı sekmeye geri döndü
    const timeAway = (Date.now() - lastVisibilityChange) / 1000;
    
    if (timeAway > 60) { // 1 dakikadan fazla uzakta kalmışsa
      showProactiveMessage("Hoş geldiniz! Size yardımcı olabilir miyim?");
      hasShownProactive = true;
    }
  }
  lastVisibilityChange = Date.now();
});
```

---

### 🎫 Ticket Yaşam Döngüsü (Ticket Lifecycle)

```
┌─────────────┐
│  📝 Yeni    │ (New) - Ticket yeni oluşturuldu
└──────┬──────┘
       │
       ↓ Agent atandı / Yanıt verildi
┌─────────────┐
│  📂 Açık    │ (Open) - Aktif olarak çalışılıyor
└──────┬──────┘
       │
       ├─→ Müşteri yanıtı bekleniyor → "Yanıt Bekleniyor"
       │
       ├─→ Dış kaynak gerekli → "Beklemede" (Pending)
       │   (Örn: Tedarikçiden bilgi bekleniyor)
       │
       ↓ Sorun çözüldü
┌─────────────┐
│ ✅ Çözüldü  │ (Resolved) - Agent çözdü işaretledi
└──────┬──────┘
       │
       ├─→ 48 saat içinde müşteri yanıt verirse → "Açık"
       │   (Tekrar açıldı - Reopened)
       │
       ↓ 48 saat geçti, yanıt yok
┌─────────────┐
│ 🔒 Kapatıldı│ (Closed) - Nihai durum
└─────────────┘

// Otomatik kapatma (cron job)
*/30 * * * * - Her 30 dakikada bir kontrol et
```

#### Ticket Status Transitions
```javascript
const ALLOWED_TRANSITIONS = {
  'new': ['open', 'pending', 'closed'],
  'open': ['waiting_reply', 'pending', 'resolved', 'closed'],
  'waiting_reply': ['open', 'resolved'],
  'pending': ['open', 'resolved'],
  'resolved': ['open', 'closed'],  // Reopen mümkün
  'closed': []  // Kapalı ticket değiştirilemez (sadece yeni ticket)
};

async function changeTicketStatus(ticketId, newStatus, agentId) {
  const ticket = await getTicket(ticketId);
  
  // 1. Geçiş kontrolü
  if (!ALLOWED_TRANSITIONS[ticket.status].includes(newStatus)) {
    throw new Error(`${ticket.status} durumundan ${newStatus}'a geçiş yapılamaz`);
  }
  
  // 2. SLA kontrolü
  if (newStatus === 'resolved') {
    await calculateSLA(ticketId);
  }
  
  // 3. Durum güncelle
  await query(`
    UPDATE tickets 
    SET status = $1, 
        updated_at = NOW(),
        resolved_at = CASE WHEN $1 = 'resolved' THEN NOW() ELSE resolved_at END,
        closed_at = CASE WHEN $1 = 'closed' THEN NOW() ELSE closed_at END
    WHERE id = $2
  `, [newStatus, ticketId]);
  
  // 4. Audit log
  await auditLog.create({
    action: 'TICKET_STATUS_CHANGE',
    target_id: ticketId,
    actor_id: agentId,
    details: {
      old_status: ticket.status,
      new_status: newStatus
    }
  });
  
  // 5. Email bildirimi
  if (newStatus === 'resolved' || newStatus === 'closed') {
    await emailService.sendTicketUpdate(ticket, newStatus);
  }
}
```

---

### ⏰ İş Saatleri ve SLA Etkisi

#### Business Hours Configuration
```javascript
// business_hours tablosu
{
  "site_id": "uuid",
  "day_of_week": 1, // 0=Pazar, 1=Pazartesi, ..., 6=Cumartesi
  "is_working_day": true,
  "start_time": "09:00",
  "end_time": "18:00",
  "break_start": "12:00",
  "break_end": "13:00"
}

// Tatil günleri (holidays tablosu)
{
  "site_id": "uuid",
  "date": "2026-10-29", // Cumhuriyet Bayramı
  "name": "Cumhuriyet Bayramı",
  "is_working": false
}
```

#### SLA Calculation with Business Hours
```javascript
async function calculateSLADueDate(ticketId, priority) {
  const ticket = await getTicket(ticketId);
  const slaHours = SLA_HOURS[priority]; // Örn: Acil=1, Yüksek=4, Normal=8, Düşük=24
  
  let dueDate = new Date(ticket.created_at);
  let remainingHours = slaHours;
  
  while (remainingHours > 0) {
    // 1. Hafta sonu kontrolü
    if (dueDate.getDay() === 0 || dueDate.getDay() === 6) {
      dueDate.setDate(dueDate.getDate() + 1);
      dueDate.setHours(9, 0, 0, 0);
      continue;
    }
    
    // 2. Tatil kontrolü
    if (await isHoliday(ticket.site_id, dueDate)) {
      dueDate.setDate(dueDate.getDate() + 1);
      dueDate.setHours(9, 0, 0, 0);
      continue;
    }
    
    // 3. Mesai saati kontrolü
    const businessHours = await getBusinessHours(ticket.site_id, dueDate.getDay());
    
    if (dueDate.getHours() < 9) {
      // Mesai öncesi → 09:00'a ayarla
      dueDate.setHours(9, 0, 0, 0);
    } else if (dueDate.getHours() >= 18) {
      // Mesai sonrası → Ertesi gün 09:00
      dueDate.setDate(dueDate.getDate() + 1);
      dueDate.setHours(9, 0, 0, 0);
      continue;
    } else if (dueDate.getHours() >= 12 && dueDate.getHours() < 13) {
      // Öğle arası → 13:00'e ayarla
      dueDate.setHours(13, 0, 0, 0);
    }
    
    // 4. Saat ekle
    dueDate.setHours(dueDate.getHours() + 1);
    remainingHours--;
  }
  
  return dueDate;
}

// Örnek:
// Cuma 17:30'da açılan "Acil" (1 saat SLA) ticket
// → Pazartesi 09:30'da due date
```

#### SLA Monitoring (Cron Job)
```javascript
// Her 5 dakikada bir kontrol
cron.schedule('*/5 * * * *', async () => {
  const now = new Date();
  
  // SLA'sı dolmak üzere olan ticket'lar (son 15 dakika)
  const aboutToBreachTickets = await query(`
    SELECT * FROM tickets
    WHERE status NOT IN ('closed', 'resolved')
      AND sla_due_date > NOW()
      AND sla_due_date <= NOW() + INTERVAL '15 minutes'
      AND sla_breach_notified = false
  `);
  
  for (const ticket of aboutToBreachTickets) {
    // Agent'a uyarı gönder
    await notificationService.send(ticket.agent_id, {
      type: 'sla_warning',
      message: `Ticket #${ticket.ticket_number} SLA'sı 15 dakika içinde dolacak!`,
      ticket_id: ticket.id
    });
    
    // Sadece bir kez uyar
    await query(`
      UPDATE tickets 
      SET sla_breach_notified = true 
      WHERE id = $1
    `, [ticket.id]);
  }
  
  // SLA'sı dolmuş ticket'lar
  const breachedTickets = await query(`
    SELECT * FROM tickets
    WHERE status NOT IN ('closed', 'resolved')
      AND sla_due_date < NOW()
      AND sla_breached = false
  `);
  
  for (const ticket of breachedTickets) {
    // İhlal olarak işaretle
    await query(`
      UPDATE tickets 
      SET sla_breached = true,
          sla_breach_time = NOW()
      WHERE id = $1
    `, [ticket.id]);
    
    // Admin'e rapor
    await notificationService.sendToAdmins(ticket.site_id, {
      type: 'sla_breach',
      message: `Ticket #${ticket.ticket_number} SLA ihlal edildi!`,
      ticket_id: ticket.id
    });
  }
});
```

---

### 📧 Email Entegrasyonu Akışı

#### IMAP - Gelen Email → Ticket
```javascript
// Email listener (IMAP)
const Imap = require('imap');

const imap = new Imap({
  user: process.env.IMAP_USER,
  password: process.env.IMAP_PASS,
  host: 'imap.gmail.com',
  port: 993,
  tls: true
});

imap.once('ready', () => {
  imap.openBox('INBOX', false, () => {
    // Yeni email geldiğinde
    imap.on('mail', async (numNewMsgs) => {
      const messages = await fetchNewMessages();
      
      for (const msg of messages) {
        await processIncomingEmail(msg);
      }
    });
  });
});

async function processIncomingEmail(email) {
  // 1. Email'i parse et
  const parsed = await parseEmail(email.raw);
  
  // 2. Hangi site'a ait? (To: address'e göre)
  // support@site1.com → Site 1
  const site = await getSiteByEmail(parsed.to);
  
  // 3. Mevcut ticket'ın yanıtı mı?
  const ticketMatch = parsed.subject.match(/#(\d+)/);
  
  if (ticketMatch) {
    // Var olan ticket'a yanıt ekle
    const ticketNumber = ticketMatch[1];
    await addTicketReply(ticketNumber, {
      from: parsed.from,
      body: parsed.text,
      attachments: parsed.attachments
    });
  } else {
    // Yeni ticket oluştur
    const ticket = await createTicket({
      site_id: site.id,
      subject: parsed.subject,
      message: parsed.text,
      visitor_email: parsed.from,
      visitor_name: parsed.fromName,
      source: 'email',
      priority: detectPriority(parsed.text), // AI ile aciliyet tespiti
      attachments: parsed.attachments
    });
    
    // Onay maili gönder
    await sendAutoReply(parsed.from, ticket);
  }
}

// Örnek onay maili
function sendAutoReply(to, ticket) {
  return emailService.send({
    to,
    subject: `[Ticket #${ticket.ticket_number}] Talebiniz alındı`,
    html: `
      <p>Sayın ${ticket.visitor_name},</p>
      <p>Talebiniz başarıyla alınmıştır.</p>
      <p><strong>Ticket Numarası:</strong> #${ticket.ticket_number}</p>
      <p><strong>Konu:</strong> ${ticket.subject}</p>
      <p>En kısa sürede size dönüş yapılacaktır.</p>
      <p>Destek Ekibi</p>
    `
  });
}
```

#### SMTP - Ticket Güncellemesi → Email
```javascript
// Ticket yanıtlandığında otomatik email
async function onTicketReply(ticketId, reply) {
  const ticket = await getTicket(ticketId);
  const visitor = await getVisitor(ticket.visitor_id);
  
  if (visitor.email) {
    await emailService.send({
      to: visitor.email,
      subject: `[Ticket #${ticket.ticket_number}] Yeni Yanıt`,
      html: emailTemplates.ticketReply({
        ticket,
        reply,
        replyUrl: `${process.env.FRONTEND_URL}/tickets/${ticket.id}`
      })
    });
  }
}

// Email şablonu
const ticketReply = ({ ticket, reply }) => `
<!DOCTYPE html>
<html>
<body style="font-family: Arial, sans-serif;">
  <div style="max-width: 600px; margin: 0 auto; padding: 20px;">
    <h2>Ticket #${ticket.ticket_number} - Yeni Yanıt</h2>
    
    <div style="background: #f5f5f5; padding: 15px; border-radius: 5px;">
      <p><strong>${reply.agent_name}</strong> yanıtladı:</p>
      <p>${reply.body}</p>
    </div>
    
    <p style="margin-top: 20px;">
      <a href="${reply.replyUrl}" 
         style="background: #4F46E5; color: white; padding: 10px 20px; 
                text-decoration: none; border-radius: 5px;">
        Ticket'ı Görüntüle
      </a>
    </p>
    
    <p style="color: #666; font-size: 12px; margin-top: 30px;">
      Bu email'e yanıt vererek doğrudan ticket'a yanıt gönderebilirsiniz.
    </p>
  </div>
</body>
</html>
`;
```

---

### 📝 Dinamik Form Akışı

#### Form Submission → Ticket Conversion
```javascript
// Widget'tan form gönderimi
async function handleFormSubmission(formData, siteId) {
  // 1. Form definition'ı getir
  const form = await getDynamicForm(formData.formId);
  
  // 2. Validasyon
  const validationErrors = validateForm(formData, form.fields);
  if (validationErrors.length > 0) {
    return { success: false, errors: validationErrors };
  }
  
  // 3. File upload'ları işle
  const attachments = [];
  for (const file of formData.files) {
    const uploaded = await uploadFile(file);
    attachments.push(uploaded);
  }
  
  // 4. Form submission kaydet
  const submission = await query(`
    INSERT INTO form_submissions (form_id, site_id, data, submitted_at)
    VALUES ($1, $2, $3, NOW())
    RETURNING id
  `, [form.id, siteId, JSON.stringify(formData)]);
  
  // 5. Ticket'a dönüştür (eğer form ayarında işaretliyse)
  if (form.create_ticket) {
    const ticket = await createTicket({
      site_id: siteId,
      subject: formData.subject || form.name,
      message: formatFormDataAsMessage(formData, form),
      visitor_name: formData.name,
      visitor_email: formData.email,
      visitor_phone: formData.phone,
      department_id: form.department_id,
      category_id: form.category_id,
      priority: form.default_priority || 'normal',
      custom_fields: formData,
      attachments,
      source: 'dynamic_form',
      form_submission_id: submission.rows[0].id
    });
    
    // 6. Onay email'i gönder
    await emailService.sendFormConfirmation(formData.email, ticket);
    
    return { success: true, ticket_id: ticket.id };
  }
  
  return { success: true, submission_id: submission.rows[0].id };
}

// Form verilerini mesaj formatına dönüştür
function formatFormDataAsMessage(data, form) {
  let message = `Form Adı: ${form.name}\n\n`;
  
  form.fields.forEach(field => {
    const value = data[field.name];
    if (value) {
      message += `${field.label}: ${value}\n`;
    }
  });
  
  return message;
}
```

---

## 🏗️ Mimari ve Teknoloji Stack

### Sistem Mimarisi

```
┌─────────────────────────────────────────────────────────────────┐
│                        CLIENT LAYER                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌──────────────────┐              ┌──────────────────┐         │
│  │  Widget (Visitor) │              │ Dashboard (Agent)│         │
│  ├──────────────────┤              ├──────────────────┤         │
│  │ • Vanilla JS     │              │ • React 18       │         │
│  │ • Socket.IO      │              │ • Vite           │         │
│  │ • WebRTC         │              │ • Zustand        │         │
│  │ • Embedded       │              │ • TailwindCSS    │         │
│  └──────────────────┘              └──────────────────┘         │
│           │                                  │                   │
│           └──────────────┬───────────────────┘                   │
└──────────────────────────┼─────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│                     APPLICATION LAYER                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌────────────────────────────────────────────────────────────┐ │
│  │              Backend (Node.js + Express)                   │ │
│  ├────────────────────────────────────────────────────────────┤ │
│  │                                                            │ │
│  │  ┌────────────┐  ┌────────────┐  ┌────────────┐         │ │
│  │  │  REST API  │  │ Socket.IO  │  │   WebRTC   │         │ │
│  │  │  (Express) │  │ (WebSocket)│  │ (Signaling)│         │ │
│  │  └────────────┘  └────────────┘  └────────────┘         │ │
│  │                                                            │ │
│  │  ┌─────────────────────────────────────────────────────┐ │ │
│  │  │            Middleware Layer                         │ │ │
│  │  │  • Auth (JWT)      • Rate Limiting                 │ │ │
│  │  │  • Validation      • Error Handling                │ │ │
│  │  │  • Helmet          • CORS                          │ │ │
│  │  └─────────────────────────────────────────────────────┘ │ │
│  │                                                            │ │
│  │  ┌─────────────────────────────────────────────────────┐ │ │
│  │  │            Service Layer                            │ │ │
│  │  │  • Visitor Tracking  • Call Management             │ │ │
│  │  │  • Chat Service      • Ticket Service              │ │ │
│  │  │  • RAG Service       • Notification Service        │ │ │
│  │  │  • Email Service     • Lock Service                │ │ │
│  │  └─────────────────────────────────────────────────────┘ │ │
│  │                                                            │ │
│  └────────────────────────────────────────────────────────────┘ │
│                                                                   │
└────────────────────────────────┬──────────────────────────────────┘
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                        DATA LAYER                                │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐          │
│  │  PostgreSQL  │  │    Redis     │  │    Ollama    │          │
│  │    (DB)      │  │   (Cache)    │  │     (AI)     │          │
│  ├──────────────┤  ├──────────────┤  ├──────────────┤          │
│  │ • pgvector   │  │ • Sessions   │  │ • llama3.1   │          │
│  │ • HNSW Index │  │ • Pub/Sub    │  │ • Embeddings │          │
│  │ • 61 Tables  │  │ • Locks      │  │ • Streaming  │          │
│  │ • 244 Index  │  │ • Queue      │  │ • Offline    │          │
│  └──────────────┘  └──────────────┘  └──────────────┘          │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Teknoloji Stack

#### Backend
```yaml
Runtime:
  - Node.js 18+
  - Express.js 4.18

Real-time:
  - Socket.IO 4.6
  - @socket.io/redis-adapter (Horizontal scaling)
  
Security:
  - jsonwebtoken (JWT)
  - bcrypt (Password hashing)
  - helmet (Security headers)
  - express-rate-limit (DDoS protection)
  - hpp (HTTP Parameter Pollution)
  - cors (Cross-origin control)

Validation:
  - joi (Schema validation)
  - express-validator

AI/RAG:
  - Ollama (Yerel LLM - llama3.1, gemma, mistral, phi3)
  - OpenAI API (GPT-4, GPT-3.5)
  - Anthropic Claude API
  - Google Gemini API
  - Azure OpenAI
  - nomic-embed-text (Embeddings - her zaman yerel)
  - pdf-parse (PDF extraction)

Email:
  - nodemailer (SMTP/IMAP)
  
Utils:
  - winston (Logging)
  - winston-daily-rotate-file (Log rotation)
  - node-cron (Scheduled tasks)
  - multer (File upload)
```

#### Frontend (Dashboard)
```yaml
Framework:
  - React 18
  - Vite 4
  
Routing:
  - React Router 6

State Management:
  - Zustand

UI:
  - TailwindCSS 3
  - HeadlessUI
  - React Icons
  
Charts:
  - Recharts (Analytics)
  
Forms:
  - React Hook Form
  
Rich Text:
  - Markdown rendering
  - Code highlighting
  
Real-time:
  - Socket.IO Client

WebRTC:
  - Native WebRTC API
```

#### Frontend (Widget)
```yaml
Core:
  - Vanilla JavaScript
  - No dependencies
  
Real-time:
  - Socket.IO Client
  
WebRTC:
  - getUserMedia
  - getDisplayMedia
  - RTCPeerConnection
  
Size:
  - ~50KB minified
```

#### Database
```yaml
Primary:
  - PostgreSQL 15
  - pgvector extension (Vector search)
  - HNSW indexing
  
Cache:
  - Redis 7
  - Redis Pub/Sub (Socket.IO adapter)
  - Redis Streams (Queue)
  
Storage:
  - Local filesystem (uploads)
  - S3-compatible (opsiyonel)
```

#### AI/ML
```yaml
LLM (Esnek Seçim):
  Yerel (Offline):
    - Ollama
    - Modeller: llama3.1:8b, gemma:2b, mistral:7b, phi3
    
  API (Cloud):
    - OpenAI (GPT-4, GPT-3.5 Turbo)
    - Anthropic (Claude 3 Sonnet, Opus)
    - Google (Gemini Pro - ücretsiz tier)
    - Azure OpenAI (Kurumsal)
  
Embeddings:
  - nomic-embed-text (Ollama - her zaman yerel)
  - 768 dimensions
  - ~100 token/saniye
  
Vector DB:
  - pgvector + HNSW indexing
  - Cosine similarity
  - ~10ms query time
```

#### DevOps
```yaml
Containerization:
  - Docker
  - Docker Compose

Web Server:
  - Nginx (Reverse proxy)
  - SSL/TLS termination

Process Manager:
  - PM2 (opsiyonel)

Monitoring:
  - Winston logging
  - Custom metrics endpoint
```

---

## 🚀 Hızlı Kurulum (Docker)

### Gereksinimler

```yaml
Düşük Donanım (Gemma 2B ile):
  CPU: 2 core
  RAM: 4 GB
  Disk: 10 GB SSD
  OS: Linux, macOS, Windows (WSL2)
  Not: API kullanımı için yeterli (Ollama olmadan)

Minimum (Llama 3.1:8B ile):
  CPU: 4 core
  RAM: 8 GB
  Disk: 20 GB SSD
  OS: Linux (Ubuntu 20.04+), macOS, Windows (WSL2)

Önerilen (Llama 3.1:8B + Yüksek trafik):
  CPU: 8 core
  RAM: 16 GB
  Disk: 50 GB SSD
  OS: Linux

Yüksek Performans (Llama 3.1:70B):
  CPU: 16 core
  RAM: 64 GB
  Disk: 100 GB SSD
  GPU: NVIDIA (Opsiyonel - 10x hızlanma)

Yazılım:
  - Docker 20.10+
  - Docker Compose 2.0+
  - Git

Alternatif (API Kullanımı):
  CPU: 2 core
  RAM: 2 GB
  Disk: 5 GB
  Internet: Hızlı ve stabil
  Not: Ollama container'ı kapat, OpenAI/Gemini API kullan
```

### Kurulum Adımları

#### 1. Repository'yi Klonlayın
```bash
git clone https://github.com/yourusername/AsistTR.git
cd AsistTR
```

#### 2. Ortam Değişkenlerini Yapılandırın
```bash
# Backend .env oluştur
cp backend/.env.example backend/.env

# Güvenli secret'lar üret
node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"

# .env dosyasını düzenle
nano backend/.env
```

**`.env` Örneği:**
```env
# Database
DB_HOST=postgres
DB_PORT=5432
DB_USER=asistr_user
DB_PASSWORD=GUVENLI_SIFRE_BURAYA
DB_NAME=asistr_db

# Redis
REDIS_HOST=redis
REDIS_PORT=6379
REDIS_PASSWORD=REDIS_SIFRESI_BURAYA

# JWT
JWT_SECRET=64_KARAKTERLIK_GUVENLI_SECRET
JWT_EXPIRATION=7d

# Server
NODE_ENV=production
PORT=4000
FRONTEND_URL=http://localhost:3000

# Email (SMTP)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=YOUR_APP_PASSWORD
SMTP_FROM=noreply@asisttr.com

# Ollama
OLLAMA_URL=http://ollama:11434
OLLAMA_MODEL=llama3.1:8b

# Rate Limiting
RATE_LIMIT_WINDOW=15
RATE_LIMIT_MAX=500

# Session
SESSION_SECRET=64_KARAKTERLIK_SESSION_SECRET
```

#### 3. Docker Compose Güncelleme
```bash
# docker-compose.yml içinde hardcoded secret'ları temizle
nano docker-compose.yml
```

**Güncellenmiş `docker-compose.yml`:**
```yaml
version: '3.8'

services:
  postgres:
    image: postgres:15-alpine
    container_name: asistr_postgres
    environment:
      POSTGRES_USER: ${DB_USER}
      POSTGRES_PASSWORD: ${DB_PASSWORD}
      POSTGRES_DB: ${DB_NAME}
    volumes:
      - postgres_data:/var/lib/postgresql/data
    ports:
      - "5432:5432"
    healthcheck:
      test: ["CMD-SHELL", "pg_isready -U ${DB_USER}"]
      interval: 10s
      timeout: 5s
      retries: 5

  redis:
    image: redis:7-alpine
    container_name: asistr_redis
    command: redis-server --requirepass ${REDIS_PASSWORD}
    ports:
      - "6379:6379"
    volumes:
      - redis_data:/data

  ollama:
    image: ollama/ollama:latest
    container_name: asistr_ollama
    volumes:
      - ollama_data:/root/.ollama
    deploy:
      resources:
        limits:
          memory: 6G
        reservations:
          memory: 4G

  backend:
    build: ./backend
    container_name: asistr_backend
    env_file:
      - ./backend/.env
    ports:
      - "4000:4000"
    depends_on:
      - postgres
      - redis
      - ollama
    volumes:
      - ./backend:/app
      - /app/node_modules

  dashboard:
    build: ./frontend/dashboard
    container_name: asistr_dashboard
    ports:
      - "3000:80"
    depends_on:
      - backend

  widget:
    build: ./frontend/widget
    container_name: asistr_widget
    ports:
      - "5173:80"
    depends_on:
      - backend

volumes:
  postgres_data:
  redis_data:
  ollama_data:
```

#### 4. Sistemitart Edin
```bash
# Tüm servisleri başlat
docker-compose up -d

# Logları izle
docker-compose logs -f
```

#### 5. Veritabanını Hazırlayın
```bash
# PostgreSQL'de pgvector extension ve şema oluştur
docker exec -i asistr_postgres psql -U asistr_user -d asistr_db < backend/init-complete-schema.sql
```

#### 6. AI Modelini Seçin ve İndirin

**Seçenek A: Düşük Donanım (2-4GB RAM)**
```bash
# Gemma 2B - En hafif model (1.4GB)
docker exec -it asistr_ollama ollama pull gemma:2b

# Embedding modeli (zorunlu)
docker exec -it asistr_ollama ollama pull nomic-embed-text

# .env'de model değiştir
nano backend/.env
# OLLAMA_MODEL=gemma:2b
```

**Seçenek B: Orta Donanım (8GB+ RAM) - Önerilen**
```bash
# Llama 3.1:8B - Dengeli model (4.7GB)
docker exec -it asistr_ollama ollama pull llama3.1:8b

# Embedding modeli
docker exec -it asistr_ollama ollama pull nomic-embed-text

# .env'de model değiştir
# OLLAMA_MODEL=llama3.1:8b (varsayılan)
```

**Seçenek C: Yüksek Donanım (40GB+ RAM)**
```bash
# Llama 3.1:70B - En kaliteli (39GB)
docker exec -it asistr_ollama ollama pull llama3.1:70b

# Embedding modeli
docker exec -it asistr_ollama ollama pull nomic-embed-text

# .env'de model değiştir
# OLLAMA_MODEL=llama3.1:70b
```

**Seçenek D: API Kullanımı (Donanım gerektirmez)**
```bash
# Ollama container'ı kapat (ihtiyaç yok)
docker-compose stop ollama

# .env'de API ayarla
nano backend/.env

# OpenAI için:
AI_PROVIDER=openai
OPENAI_API_KEY=sk-proj-...
OPENAI_MODEL=gpt-4-turbo

# Veya Google Gemini (ücretsiz):
AI_PROVIDER=google
GOOGLE_API_KEY=AIzaSy...
GOOGLE_MODEL=gemini-pro
```

#### 7. İlk Kullanıcıyı Oluşturun
```bash
# Backend container'a gir
docker exec -it asistr_backend npm run seed:admin

# Veya manuel:
docker exec -it asistr_backend node scripts/create-admin.js
```

#### 8. Erişim
```
Dashboard: http://localhost:3000
Backend API: http://localhost:4000
Widget: http://localhost:5173

İlk Giriş:
Email: admin@asisttr.com
Password: admin123 (hemen değiştirin!)
```

---

## ⚙️ Yapılandırma

### Dashboard Konfigürasyonu

**`frontend/dashboard/.env`:**
```env
VITE_API_URL=http://localhost:4000
VITE_WS_URL=ws://localhost:4000
VITE_VAPID_PUBLIC_KEY=YOUR_VAPID_PUBLIC_KEY
```

### Widget Konfigürasyonu

Widget statik olarak build edilir ve CDN'e yüklenir:

```bash
cd frontend/widget
npm run build

# Build çıktısı: dist/widget.js
# Bu dosyayı CDN'e veya Nginx'e kopyalayın
```

### Nginx Yapılandırması (Production)

**`/etc/nginx/sites-available/asisttr`:**
```nginx
# API ve WebSocket
server {
    listen 443 ssl http2;
    server_name api.asisttr.com;

    ssl_certificate /etc/letsencrypt/live/asisttr.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/asisttr.com/privkey.pem;

    # Security Headers
    add_header Strict-Transport-Security "max-age=31536000; includeSubDomains" always;
    add_header X-Frame-Options DENY always;
    add_header X-Content-Type-Options nosniff always;
    add_header X-XSS-Protection "1; mode=block" always;

    # Backend API
    location /api/ {
        proxy_pass http://localhost:4000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_cache_bypass $http_upgrade;
    }

    # WebSocket
    location /socket.io/ {
        proxy_pass http://localhost:4000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_set_header Host $host;
        proxy_read_timeout 86400;
    }

    # Gzip
    gzip on;
    gzip_types text/plain application/json application/javascript text/css;
    gzip_min_length 1000;
}

# Dashboard
server {
    listen 443 ssl http2;
    server_name dashboard.asisttr.com;

    ssl_certificate /etc/letsencrypt/live/asisttr.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/asisttr.com/privkey.pem;

    root /var/www/asisttr/dashboard;
    index index.html;

    location / {
        try_files $uri $uri/ /index.html;
    }

    gzip on;
    gzip_types text/plain text/css application/javascript;
}

# Widget CDN
server {
    listen 443 ssl http2;
    server_name cdn.asisttr.com;

    ssl_certificate /etc/letsencrypt/live/asisttr.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/asisttr.com/privkey.pem;

    root /var/www/asisttr/widget;

    # CORS for widget
    add_header Access-Control-Allow-Origin * always;
    add_header Access-Control-Allow-Methods "GET, OPTIONS" always;

    location /widget.js {
        expires 1h;
        add_header Cache-Control "public, immutable";
    }
}
```

---

## 🔐 Güvenlik

### İmplementasyonlar

#### 1. Authentication & Authorization
```javascript
// JWT Middleware
const authMiddleware = async (req, res, next) => {
  const token = req.header('Authorization')?.replace('Bearer ', '');
  
  if (!token) {
    return res.status(401).json({ error: 'Token bulunamadı' });
  }
  
  try {
    const decoded = jwt.verify(token, process.env.JWT_SECRET);
    const user = await getUserById(decoded.id);
    
    if (!user || !user.is_active) {
      return res.status(401).json({ error: 'Geçersiz kullanıcı' });
    }
    
    req.user = user;
    next();
  } catch (error) {
    return res.status(401).json({ error: 'Geçersiz token' });
  }
};

// Role-based middleware
const adminOnly = (req, res, next) => {
  if (req.user.role !== 'admin' && req.user.role !== 'superadmin') {
    return res.status(403).json({ error: 'Yetkiniz yok' });
  }
  next();
};

const agentOrAdmin = (req, res, next) => {
  if (req.user.role === 'agent') {
    // Agent sadece kendi sitesine erişebilir
    req.siteFilter = { site_id: req.user.site_id };
  }
  next();
};
```

#### 2. Rate Limiting
```javascript
const rateLimit = require('express-rate-limit');

// Genel limiter
const generalLimiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 dakika
  max: 500,
  message: 'Çok fazla istek gönderdiniz'
});

// Auth limiter (brute force protection)
const authLimiter = rateLimit({
  windowMs: 60 * 60 * 1000, // 1 saat
  max: 5,
  skipSuccessfulRequests: true,
  message: 'Çok fazla giriş denemesi'
});

app.use('/api/', generalLimiter);
app.use('/api/auth/', authLimiter);
```

#### 3. Input Sanitization
```javascript
const sanitize = require('express-mongo-sanitize');
const xss = require('xss-clean');
const hpp = require('hpp');

app.use(sanitize()); // NoSQL injection
app.use(xss());      // XSS
app.use(hpp());      // HTTP Parameter Pollution
```

#### 4. Helmet Security Headers
```javascript
const helmet = require('helmet');

app.use(helmet({
  contentSecurityPolicy: {
    directives: {
      defaultSrc: ["'self'"],
      scriptSrc: ["'self'", "'unsafe-inline'", "cdn.asisttr.com"],
      styleSrc: ["'self'", "'unsafe-inline'"],
      imgSrc: ["'self'", "data:", "https:"],
      connectSrc: ["'self'", "wss:", "https:"],
      frameSrc: ["'none'"],
      objectSrc: ["'none'"]
    }
  },
  hsts: {
    maxAge: 31536000,
    includeSubDomains: true,
    preload: true
  }
}));
```

#### 5. CORS Configuration
```javascript
const cors = require('cors');

app.use(cors({
  origin: function(origin, callback) {
    const allowedOrigins = [
      'http://localhost:3000',
      'http://localhost:5173',
      'https://dashboard.asisttr.com',
      'https://cdn.asisttr.com'
    ];
    
    if (!origin || allowedOrigins.indexOf(origin) !== -1) {
      callback(null, true);
    } else {
      callback(new Error('CORS policy violation'));
    }
  },
  credentials: true
}));
```

#### 6. SQL Injection Protection
```javascript
// ❌ YANLIŞ (vulnerable)
const query = `SELECT * FROM users WHERE email = '${email}'`;

// ✅ DOĞRU (safe)
const query = 'SELECT * FROM users WHERE email = $1';
const result = await pool.query(query, [email]);
```

#### 7. File Upload Security
```javascript
const multer = require('multer');
const path = require('path');
const FileType = require('file-type');

const storage = multer.diskStorage({
  destination: './uploads/',
  filename: (req, file, cb) => {
    const uniqueName = `${Date.now()}-${Math.random().toString(36)}${path.extname(file.originalname)}`;
    cb(null, uniqueName);
  }
});

const fileFilter = async (req, file, cb) => {
  // Boyut kontrolü (10MB)
  if (file.size > 10 * 1024 * 1024) {
    return cb(new Error('Dosya çok büyük (max 10MB)'));
  }
  
  // MIME type kontrolü
  const allowedMimes = ['image/jpeg', 'image/png', 'application/pdf'];
  if (!allowedMimes.includes(file.mimetype)) {
    return cb(new Error('Geçersiz dosya tipi'));
  }
  
  cb(null, true);
};

const upload = multer({ 
  storage,
  fileFilter,
  limits: { fileSize: 10 * 1024 * 1024 }
});

// Magic bytes kontrolü (post-upload)
app.post('/upload', upload.single('file'), async (req, res) => {
  const fileType = await FileType.fromFile(req.file.path);
  
  if (!fileType || !['image/jpeg', 'image/png', 'application/pdf'].includes(fileType.mime)) {
    fs.unlinkSync(req.file.path); // Sahte dosyayı sil
    return res.status(400).json({ error: 'Geçersiz dosya' });
  }
  
  res.json({ success: true, file: req.file });
});
```

---

## 📊 Veritabanı Şeması

### Tablo Listesi (61 Tablo)

```sql
-- Core Tables
users                    -- Admin/Agent kullanıcılar
sites                    -- Kayıtlı web siteleri
visitors                 -- Ziyaretçiler
visitor_sessions         -- Ziyaretçi oturum geçmişi

-- Messaging
conversations            -- Sohbet oturumları
messages                 -- Mesajlar
conversation_notes       -- Dahili notlar
message_reactions        -- Mesaj tepkileri

-- Tickets
tickets                  -- Ticket'lar
ticket_replies           -- Ticket yanıtları
ticket_categories        -- Ticket kategorileri
ticket_templates         -- Ticket şablonları
ticket_locks             -- Ticket kilitleri
ticket_attachments       -- Ticket ekleri

-- RAG/AI
knowledge_base           -- Bilgi tabanı
embeddings               -- Vector embeddings
chat_tags                -- Sohbet etiketleri
canned_responses         -- Hazır yanıtlar

-- Organization
departments              -- Departmanlar
teams                    -- Takımlar
team_members             -- Takım üyeleri
agent_skills             -- Agent yetenekleri

-- Voice/Video
voice_calls              -- Sesli aramalar
call_queue               -- Arama kuyruğu
call_recordings          -- Arama kayıtları

-- Forms
dynamic_forms            -- Dinamik formlar
form_submissions         -- Form gönderimleri
offline_messages         -- Offline mesajlar

-- Notifications
notifications            -- Bildirimler
notification_preferences -- Bildirim tercihleri
push_subscriptions       -- Push notification abonelikleri

-- Analytics
visitor_tracking         -- Ziyaretçi takibi
agent_metrics            -- Agent metrikleri
conversation_ratings     -- Sohbet puanlamaları

-- Settings
widget_settings          -- Widget ayarları
email_templates          -- Email şablonları
business_hours           -- İş saatleri
routing_rules            -- Yönlendirme kuralları

-- Audit & Security
audit_logs               -- Denetim logları
api_keys                 -- API anahtarları
sessions                 -- Oturum kayıtları
password_resets          -- Şifre sıfırlama tokenları

-- Presence
agents_presence          -- Agent çevrimiçi durumu
```

### Temel Tablo Şemaları

#### users
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
  site_id UUID REFERENCES sites(id) ON DELETE CASCADE,
  email VARCHAR(255) UNIQUE NOT NULL,
  password_hash VARCHAR(255),
  name VARCHAR(255) NOT NULL,
  role VARCHAR(50) NOT NULL CHECK (role IN ('superadmin', 'admin', 'agent', 'customer')),
  
  -- Agent özellikleri
  department_id UUID REFERENCES departments(id),
  skills TEXT[],
  max_chats INTEGER DEFAULT 5,
  current_chats INTEGER DEFAULT 0,
  priority_level INTEGER DEFAULT 1,
  accept_calls BOOLEAN DEFAULT true,
  
  -- Status
  is_active BOOLEAN DEFAULT true,
  is_vip BOOLEAN DEFAULT false,
  is_banned BOOLEAN DEFAULT false,
  ban_reason TEXT,
  banned_by UUID REFERENCES users(id),
  banned_at TIMESTAMP,
  
  -- Auth
  last_login TIMESTAMP,
  reset_password_token VARCHAR(255),
  reset_password_expires TIMESTAMP,
  
  -- Timestamps
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_users_site ON users(site_id);
CREATE INDEX idx_users_email ON users(email);
CREATE INDEX idx_users_role ON users(role, site_id);
```

#### visitor_sessions
```sql
CREATE TABLE visitor_sessions (
  id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
  visitor_id UUID REFERENCES visitors(id) ON DELETE CASCADE,
  session_id VARCHAR(255) NOT NULL,
  site_id UUID REFERENCES sites(id) ON DELETE CASCADE,
  
  -- Session info
  started_at TIMESTAMP NOT NULL,
  ended_at TIMESTAMP,
  total_duration_seconds INTEGER DEFAULT 0,
  
  -- Tracking data
  browser VARCHAR(100),
  os VARCHAR(100),
  device VARCHAR(50),
  country VARCHAR(100),
  city VARCHAR(100),
  ip_address INET,
  
  -- Metrics
  page_views INTEGER DEFAULT 0,
  activity_timeline JSONB,  -- [{timestamp, action, page, duration}]
  pages_visited JSONB,       -- [{url, title, visits, total_time}]
  
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_visitor_sessions_visitor ON visitor_sessions(visitor_id);
CREATE INDEX idx_visitor_sessions_site ON visitor_sessions(site_id);
CREATE INDEX idx_visitor_sessions_dates ON visitor_sessions(started_at, ended_at);
```

#### knowledge_base
```sql
CREATE TABLE knowledge_base (
  id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
  site_id UUID REFERENCES sites(id) ON DELETE CASCADE,
  title VARCHAR(500) NOT NULL,
  content TEXT NOT NULL,
  
  -- Vector search
  embedding vector(768),  -- pgvector extension
  
  -- SEO
  slug VARCHAR(255) UNIQUE,
  meta_description VARCHAR(500),
  
  -- Categorization
  category VARCHAR(100),
  tags TEXT[],
  
  -- Visibility
  status VARCHAR(50) DEFAULT 'draft' CHECK (status IN ('draft', 'published', 'archived')),
  visibility VARCHAR(50) DEFAULT 'public' CHECK (visibility IN ('public', 'internal')),
  
  -- Analytics
  views INTEGER DEFAULT 0,
  helpful_count INTEGER DEFAULT 0,
  not_helpful_count INTEGER DEFAULT 0,
  
  -- Timestamps
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  published_at TIMESTAMP
);

-- Vector search index (HNSW)
CREATE INDEX idx_knowledge_embedding ON knowledge_base 
  USING hnsw (embedding vector_cosine_ops);

-- Full-text search index
CREATE INDEX idx_knowledge_fulltext ON knowledge_base 
  USING gin(to_tsvector('turkish', title || ' ' || content));

CREATE INDEX idx_knowledge_site ON knowledge_base(site_id);
CREATE INDEX idx_knowledge_slug ON knowledge_base(slug);
```

#### audit_logs
```sql
CREATE TABLE audit_logs (
  id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
  site_id UUID REFERENCES sites(id) ON DELETE CASCADE,
  actor_id UUID REFERENCES users(id) ON DELETE SET NULL,
  
  -- Action
  action VARCHAR(50) NOT NULL,  -- 'CREATE', 'UPDATE', 'DELETE', 'LOGIN'
  target_type VARCHAR(50),      -- 'user', 'ticket', 'conversation'
  target_id UUID,
  
  -- Details
  details JSONB,
  changes JSONB,  -- {field: {old: x, new: y}}
  
  -- Request info
  ip_address INET,
  user_agent TEXT,
  
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_audit_site_date ON audit_logs(site_id, created_at DESC);
CREATE INDEX idx_audit_actor ON audit_logs(actor_id);
CREATE INDEX idx_audit_action ON audit_logs(action, target_type);
```

---

## 📚 API Dokümantasyonu

### Base URL
```
Production: https://api.asisttr.com
Development: http://localhost:4000
```

### Authentication

Tüm API istekleri (public endpoint'ler hariç) JWT token gerektirir:

```bash
curl -H "Authorization: Bearer YOUR_JWT_TOKEN" \
     https://api.asisttr.com/api/conversations
```

### Endpoints

#### Auth
```
POST   /api/auth/register       # Kayıt ol
POST   /api/auth/login          # Giriş yap
POST   /api/auth/logout         # Çıkış yap
POST   /api/auth/refresh        # Token yenile
POST   /api/auth/forgot-password
POST   /api/auth/reset-password
GET    /api/auth/me             # Mevcut kullanıcı
```

#### Conversations
```
GET    /api/chat                # Tüm sohbetler
GET    /api/chat/:id            # Tek sohbet detayı
POST   /api/chat/:id/message    # Mesaj gönder
PUT    /api/chat/:id/assign     # Agent ata
PUT    /api/chat/:id/transfer   # Sohbet devret
PUT    /api/chat/:id/close      # Sohbeti kapat
POST   /api/chat/:id/note       # Not ekle
POST   /api/chat/:id/tag        # Etiket ekle
DELETE /api/chat/:id            # Sohbet sil
```

#### Tickets
```
GET    /api/tickets             # Tüm ticketlar
GET    /api/tickets/:id         # Ticket detayı
POST   /api/tickets             # Yeni ticket
PUT    /api/tickets/:id         # Ticket güncelle
DELETE /api/tickets/:id         # Ticket sil
POST   /api/tickets/:id/reply   # Yanıt ekle
PUT    /api/tickets/:id/assign  # Agent ata
PUT    /api/tickets/:id/status  # Durum değiştir
GET    /api/tickets/:id/lock    # Kilit al
DELETE /api/tickets/:id/lock    # Kilidi bırak
```

#### Knowledge Base
```
GET    /api/knowledge           # Tüm bilgiler (admin)
GET    /api/knowledge/public    # Public bilgiler
GET    /api/knowledge/:id       # Bilgi detayı
POST   /api/knowledge           # Yeni bilgi ekle
PUT    /api/knowledge/:id       # Bilgi güncelle
DELETE /api/knowledge/:id       # Bilgi sil
POST   /api/knowledge/bulk      # Toplu ekleme
GET    /api/knowledge/search    # Arama
```

#### Visitors
```
GET    /api/tracking/visitors            # Tüm ziyaretçiler
GET    /api/tracking/visitors/:id        # Ziyaretçi detayı
GET    /api/tracking/visitors/:id/history # Gezinti geçmişi
GET    /api/tracking/visitors/:id/sessions # Oturum geçmişi
POST   /api/tracking/pageview            # Sayfa görüntüleme
```

#### Analytics
```
GET    /api/analytics/overview           # Genel özet
GET    /api/analytics/agents             # Agent performansı
GET    /api/analytics/conversations      # Sohbet analizi
GET    /api/analytics/tickets            # Ticket analizi
GET    /api/analytics/visitors           # Ziyaretçi analizi
GET    /api/analytics/funnel             # Funnel analizi
```

#### Settings
```
GET    /api/settings/widget              # Widget ayarları
PUT    /api/settings/widget              # Widget güncelle
GET    /api/settings/business-hours      # İş saatleri
PUT    /api/settings/business-hours      # İş saatleri güncelle
GET    /api/settings/routing             # Routing kuralları
PUT    /api/settings/routing             # Routing güncelle
```

### WebSocket Events

#### Client → Server
```javascript
// Widget bağlantısı
socket.emit('tracking:visitor:connect', {
  visitorId,
  sessionId,
  siteId,
  page: window.location.href
});

// Sayfa değişimi
socket.emit('tracking:pageview', {
  visitorId,
  url,
  title
});

// Mesaj gönderme
socket.emit('chat:message', {
  conversationId,
  body,
  attachments
});

// Sesli arama
socket.emit('call:initiate', {
  targetId,
  conversationId
});

// Typing indicator
socket.emit('chat:typing', {
  conversationId,
  isTyping: true
});
```

#### Server → Client
```javascript
// Yeni mesaj
socket.on('chat:message:new', (data) => {
  console.log('Yeni mesaj:', data);
});

// Agent yazıyor
socket.on('chat:typing', (data) => {
  console.log('Agent yazıyor:', data.agentName);
});

// Gelen arama
socket.on('call:incoming', (data) => {
  console.log('Gelen arama:', data);
});

// AI yanıtı (streaming)
socket.on('ai:chunk', (chunk) => {
  console.log('AI chunk:', chunk);
});

// Ziyaretçi aktivitesi
socket.on('visitor:activity', (data) => {
  console.log('Ziyaretçi:', data);
});
```

---

## 🚀 Deployment (Production)

### Hazırlık Checklist

- [ ] `.env` dosyalarında production değerleri ayarlandı
- [ ] JWT_SECRET güvenli ve uzun (64+ karakter)
- [ ] Redis şifresi ayarlandı
- [ ] SMTP ayarları yapıldı
- [ ] SSL sertifikaları hazır (Let's Encrypt)
- [ ] Domain DNS ayarları yapıldı
- [ ] Firewall kuralları belirlendi
- [ ] Backup stratejisi planlandı

### Docker Production Build

```bash
# 1. Production .env dosyalarını hazırla
cp backend/.env.example backend/.env.production
nano backend/.env.production

# 2. Docker Compose production modu
docker-compose -f docker-compose.production.yml up -d

# 3. Veritabanını kur
docker exec -i asistr_postgres psql -U asistr_user -d asistr_db < backend/init-complete-schema.sql

# 4. Ollama modelini indir
docker exec -it asistr_ollama ollama pull llama3.1:8b
docker exec -it asistr_ollama ollama pull nomic-embed-text

# 5. İlk admin kullanıcısı
docker exec -it asistr_backend npm run seed:admin
```

### Nginx SSL Setup

```bash
# 1. Certbot kur
sudo apt install certbot python3-certbot-nginx

# 2. SSL sertifikası al
sudo certbot --nginx -d asisttr.com -d www.asisttr.com \
  -d api.asisttr.com -d dashboard.asisttr.com -d cdn.asisttr.com

# 3. Auto-renewal test
sudo certbot renew --dry-run

# 4. Nginx konfigürasyonunu kopyala
sudo cp nginx/asisttr.conf /etc/nginx/sites-available/asisttr
sudo ln -s /etc/nginx/sites-available/asisttr /etc/nginx/sites-enabled/

# 5. Nginx test ve restart
sudo nginx -t
sudo systemctl restart nginx
```

### Monitoring & Logging

#### PM2 Process Manager (Opsiyonel)
```bash
# PM2 kur
npm install -g pm2

# Backend'i başlat
cd backend
pm2 start npm --name "asisttr-backend" -- start

# Auto-restart on system reboot
pm2 startup
pm2 save

# Logs
pm2 logs asisttr-backend
pm2 monit
```

#### Log Rotation
```bash
# /etc/logrotate.d/asisttr
/var/log/asisttr/*.log {
  daily
  rotate 14
  compress
  delaycompress
  notifempty
  create 0640 www-data www-data
  sharedscripts
  postrotate
    docker exec asistr_backend npm run logs:rotate
  endscript
}
```

### Backup Strategy

#### Veritabanı Yedekleme
```bash
#!/bin/bash
# backup.sh

DATE=$(date +%Y%m%d_%H%M%S)
BACKUP_DIR="/backups/postgresql"

# PostgreSQL dump
docker exec asistr_postgres pg_dump -U asistr_user asistr_db | \
  gzip > $BACKUP_DIR/backup_$DATE.sql.gz

# 30 günden eski yedekleri sil
find $BACKUP_DIR -name "*.sql.gz" -mtime +30 -delete

echo "Backup completed: backup_$DATE.sql.gz"
```

#### Cron Job
```cron
# Her gün saat 03:00'te backup
0 3 * * * /path/to/backup.sh
```

### Health Checks

```bash
# API health check
curl https://api.asisttr.com/health

# Response:
{
  "status": "ok",
  "timestamp": "2026-01-09T10:00:00Z",
  "services": {
    "database": "connected",
    "redis": "connected",
    "ollama": "running"
  },
  "uptime": 86400
}
```

### Performance Tuning

#### PostgreSQL Optimization
```sql
-- postgresql.conf
shared_buffers = 4GB
effective_cache_size = 12GB
maintenance_work_mem = 1GB
checkpoint_completion_target = 0.9
wal_buffers = 16MB
default_statistics_target = 100
random_page_cost = 1.1
effective_io_concurrency = 200
work_mem = 20MB
min_wal_size = 2GB
max_wal_size = 8GB
max_worker_processes = 8
max_parallel_workers_per_gather = 4
max_parallel_workers = 8
```

#### Redis Optimization
```conf
# redis.conf
maxmemory 2gb
maxmemory-policy allkeys-lru
save 900 1
save 300 10
save 60 10000
```

---

## 🤝 Katkıda Bulunma

Katkılarınızı bekliyoruz! Lütfen contribution guidelines'ı okuyun:

### Development Setup

```bash
# 1. Fork ve clone
git clone https://github.com/yourusername/AsistTR.git
cd AsistTR

# 2. Branch oluştur
git checkout -b feature/amazing-feature

# 3. Değişiklikleri commit et
git commit -m "feat: amazing feature eklendi"

# 4. Push
git push origin feature/amazing-feature

# 5. Pull Request aç
```

### Commit Conventions

```
feat:     Yeni özellik
fix:      Bug düzeltme
docs:     Dokümantasyon
style:    Formatting, noktalama
refactor: Kod refactoring
test:     Test ekleme/düzeltme
chore:    Bakım işleri
```


---

## 🙏 Teşekkürler

Bu proje aşağıdaki açık kaynak projeleri kullanmaktadır:

- [Node.js](https://nodejs.org/)
- [React](https://reactjs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Redis](https://redis.io/)
- [Socket.IO](https://socket.io/)
- [Ollama](https://ollama.ai/)
- [pgvector](https://github.com/pgvector/pgvector)
- [Express](https://expressjs.com/)
- [TailwindCSS](https://tailwindcss.com/)

---

<div align="center">



</div>
