## 📄 Backend Project Structure Documentation

### English Version

```
backend/
├─ cmd/
│   └─ main.go         → Entry point of the application. Starts the HTTP server.
├─ internal/
│   ├─ db/             → Database-related code, like connection setup and migrations.
│   ├─ models/         → Data models / structs representing database tables.
│   ├─ routes/         → HTTP route definitions.
│   └─ handlers/       → Route handlers, the logic executed for each endpoint.
├─ .env                → Environment variables, e.g., DB credentials, ports.
├─ go.mod              → Go module definition file.
```

**Explanation:**

* `cmd/`: Contains the main executable entry point. You can later add multiple apps or services here.
* `internal/`: Go convention for code that is private to the module. Contains DB connection, models, routes, and handlers.
* `db/`: Place for DB connection logic, migrations, and helper functions.
* `models/`: Structs representing tables or entities in the PostgreSQL database.
* `routes/`: Where you define all HTTP endpoints and attach them to handlers.
* `handlers/`: Business logic for each route. Separating handlers keeps routes clean.
* `.env`: Keeps secrets and configs out of code.
* `go.mod`: Keeps track of Go dependencies and module information.

---

### Türkçe Versiyon

```
backend/
├─ cmd/
│   └─ main.go         → Uygulamanın giriş noktası. HTTP sunucusunu başlatır.
├─ internal/
│   ├─ db/             → Veritabanı ile ilgili kodlar, bağlantı ayarları ve migrationlar.
│   ├─ models/         → Veritabanı tablolarını temsil eden veri modelleri / structlar.
│   ├─ routes/         → HTTP route tanımlamaları.
│   └─ handlers/       → Her endpoint için çalıştırılacak iş mantığı.
├─ .env                → Ortam değişkenleri, örn: DB bilgileri, portlar.
├─ go.mod              → Go modül tanım dosyası.
```

**Açıklama:**

* `cmd/`: Ana çalıştırılabilir dosya burada bulunur. Gelecekte birden fazla servis ekleyebilirsiniz.
* `internal/`: Go’da modül dışına açılmayan kodlar için kullanılan klasör. DB bağlantısı, modeller, route ve handlerlar burada yer alır.
* `db/`: Veritabanı bağlantı mantığı, migration ve yardımcı fonksiyonlar burada bulunur.
* `models/`: PostgreSQL veritabanındaki tabloları veya entity’leri temsil eden structlar.
* `routes/`: Tüm HTTP endpointlerin tanımlandığı yer ve handlerlara bağlandığı klasör.
* `handlers/`: Her route’un iş mantığı burada bulunur. Handlerları ayrı tutmak route kodlarını temiz tutar.
* `.env`: Gizli bilgiler ve config dosyalarını koddan ayırmak için kullanılır.
* `go.mod`: Go bağımlılıklarını ve modül bilgisini tutar.
