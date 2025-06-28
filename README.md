# 🎮 Game Store API v1.0

A modern RESTful API built with .NET 10 Minimal APIs for managing a game store inventory. This project demonstrates best practices for building lightweight, high-performance APIs using the latest .NET features.

> **Learning Project**: I am learning .NET 10 Minimal API from different Video Courses, Books, and Websites.

## 🚀 Features

- ✅ **CRUD Operations**: Complete Create, Read, Update, Delete functionality for games
- ✅ **In-Memory Storage**: Fast in-memory data store for development and testing
- ✅ **Data Validation**: Comprehensive input validation with custom error messages
- ✅ **OpenAPI Integration**: Full Swagger/OpenAPI 3.0 specification support
- ✅ **Modern Documentation**: Beautiful Scalar UI for API exploration
- ✅ **RESTful Design**: Follows REST architectural principles
- ✅ **Status Code Handling**: Proper HTTP status codes for all scenarios
- ✅ **Type Safety**: Strongly typed models and responses

## 🛠️ Tech Stack

- **Framework**: .NET 10 (Preview)
- **API Style**: Minimal APIs
- **Documentation**: OpenAPI 3.0 + Scalar UI
- **Validation**: Data Annotations + MinimalApis.Extensions
- **Testing**: xUnit (Unit Tests)

## 📋 API Endpoints

| Method | Endpoint      | Description          | Status Codes       |
| ------ | ------------- | -------------------- | ------------------ |
| GET    | `/`           | Welcome message      | 200                |
| GET    | `/games`      | Get all games        | 200, 500           |
| GET    | `/games/{id}` | Get game by ID       | 200, 404, 500      |
| POST   | `/games`      | Create new game      | 201, 400, 500      |
| PUT    | `/games/{id}` | Update existing game | 204, 400, 404, 500 |
| DELETE | `/games/{id}` | Delete game          | 204, 404, 500      |

## 🏃‍♂️ Quick Start

### Prerequisites

- [.NET 10 SDK](https://dotnet.microsoft.com/download) (Preview)
- Your favorite IDE (Visual Studio, VS Code, Rider)

### Running the API

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd gamestore-api-v1.0
   ```

2. **Restore dependencies**

   ```bash
   dotnet restore
   ```

3. **Run the application**

   ```bash
   dotnet run --project src/GameStore.Api
   ```

   **Or for development with hot reload:**

   ```bash
   dotnet watch --project .\src\GameStore.Api\
   ```

4. **Access the API**

   - API Base URL: `https://localhost:7011`
   - Scalar Documentation: `https://localhost:7011/scalar/v1`
   - OpenAPI Spec: `https://localhost:7011/openapi/v1.json`

## 📚 Documentation & Testing

### Interactive Documentation

The API includes a beautiful, modern documentation interface powered by Scalar UI:

![Scalar UI](./docs/images/Scalar_V1.PNG)

### Available Documentation

- **Scalar UI**: Modern, interactive API documentation at `/scalar/v1`
- **OpenAPI Spec**: Machine-readable specification at `/openapi/v1.json`
- **HTTP File**: Ready-to-use requests in `src/GameStore.Api/gamestore.http`

### Sample Game Object

```json
{
  "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "name": "Street Fighter II",
  "genre": "Fighting",
  "price": 19.99,
  "releaseDate": "1992-07-15"
}
```

## 🧪 Testing

### Using the HTTP File

Open `src/GameStore.Api/gamestore.http` in VS Code and execute the pre-configured requests.

### Using Scalar UI

1. Navigate to `https://localhost:7011/scalar/v1`
2. Explore endpoints and try them directly in the browser
3. View request/response examples and schemas

### Unit Tests

```bash
dotnet test
```

## 📁 Project Structure

```text
gamestore-api-v1.0/
├── src/
│   └── GameStore.Api/
│       ├── Models/
│       │   ├── Game.cs           # Game entity model
│       │   └── Genre.cs          # Genre entity model
│       ├── Program.cs            # API configuration and endpoints
│       ├── gamestore.http        # HTTP requests for testing
│       └── GameStore.Api.csproj  # Project file
├── tests/
│   └── GameStore.Api.UnitTests/  # Unit test project
├── docs/
│   ├── v1.0-Basic-In-Memory-API.md  # Detailed documentation
│   └── images/                   # Documentation images
├── Directory.Build.props         # Build configuration settings
├── Directory.Packages.props      # Centralized package management
├── gamestore-api-v1.0.sln        # Solution file
├── LICENSE                       # License file
└── README.md                     # This file
```

## 📋 To Do

- [ ] Implement error handling
- [ ] Implement logging and monitoring
- [ ] Add comprehensive unit tests
- [ ] Add integration tests
- [ ] Implement database persistence
- [ ] Add authentication and authorization
- [ ] Add API versioning
- [ ] Implement caching
- [ ] Add health checks
- [ ] Docker containerization

## 🤝 Contributing

This is a learning project, but feel free to:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

This project is for educational purposes. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- .NET Team for the amazing Minimal APIs
- Scalar team for the beautiful API documentation UI
- Various online courses, books, and tutorials that helped in learning
