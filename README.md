# QuizServer Projesi

QuizServer, kullanıcıların çeşitli quizler oluşturup yönetebileceği bir uygulamadır. Proje, hem sunucu (backend) hem de istemci (frontend) tarafını içermekte ve .NET Core ile Angular kullanılarak geliştirilmiştir.

## Proje Yapısı

### 1. QuizServer (Backend)
#### a. QuizServer.Application
- **Application Katmanı**: Uygulamanın iş mantığını içerir.
  - **Auth, QuizDetails, QuizPages, Quizzes, Services**: Uygulamanın çeşitli iş mantığı özelliklerini içerir.
  - **MediatR**: CQRS desenini uygulamak için kullanılır.
  - **TS.Result**: İşlemlerin sonuçlarını yönetmek için kullanılır.

#### b. QuizServer.Domain
- **Domain Katmanı**: Uygulamanın çekirdek iş mantığı ve kurallarını içerir.
  - **Entities**: Quiz, QuizDetails, Users, Shared gibi temel veritabanı varlıklarını içerir.
  - **Dtos**: Veri transfer nesneleri.
  - **Shared**: Uygulama genelinde kullanılacak ortak yapılar.

#### c. QuizServer.Infrastructure
- **Infrastructure Katmanı**: Uygulamanın altyapı hizmetlerini sağlar.
  - **Configurations, Context, Repositories, Services**: Veritabanı ve diğer altyapı işlemlerini yönetir.
  - **Entity Framework Core**: Veritabanı işlemleri için kullanılır.
  - **HealthChecks**: Uygulama sağlığını izlemek için kullanılır.
  - **Scrutor**: Bağımlılık çözümlemesi için kullanılır.

#### d. QuizServer.WebAPI
- **WebAPI Katmanı**: Uygulamanın dış dünya ile etkileşime geçtiği katmandır.
  - **Controllers**: HTTP isteklerini işleyen denetleyiciler.
  - **Middleware**: İsteklerin işlenmesi sırasında kullanılan ara yazılımlar.
  - **Swagger (Swashbuckle)**: API dokümantasyonu sağlar.

#### e. QuizServer.ConsoleApp
- **ConsoleApp Katmanı**: Konsol tabanlı yardımcı araçlar ve işlemler için geliştirilmiştir.

#### f. QuizServer.HeathCheck.WebAPI
- **HealthCheck WebAPI**: Uygulamanın sağlığını izlemek ve raporlamak için kullanılır.

### 2. QuizClient (Frontend)
- **Angular** ile geliştirilmiş kullanıcı arayüzüdür.
- **Flexi-grid** ve **Flexi-toast** gibi kütüphaneler ile zengin bir kullanıcı deneyimi sağlar.
- **@microsoft/signalr** ile gerçek zamanlı iletişim sağlanır.
- JWT tabanlı kimlik doğrulama için **jwt-decode** kullanılır.

## Kullanılan Teknolojiler ve Kütüphaneler
### Backend
- **ASP.NET Core**
- **Entity Framework Core**
- **MediatR**
- **TS.Result**
- **Scrutor**
- **HealthChecks**
- **Swagger (Swashbuckle)**

### Frontend
- **Angular**
- **Flexi-grid**
- **Flexi-toast**
- **@microsoft/signalr**
- **jwt-decode**
