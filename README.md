# 🛍️ nopCommerce Local Setup

This repository contains a local working copy of **nopCommerce 4.90** for testing and automation purposes.

---

## ⚙️ Requirements
- [.NET 9 SDK (x64)](https://dotnet.microsoft.com/en-us/download)
- [SQL Server Express or LocalDB](https://learn.microsoft.com/en-us/sql/database-engine/configure-windows/sql-server-express-localdb)
- (Optional) [Visual Studio 2022](https://visualstudio.microsoft.com/vs/)  
  *(with ASP.NET and web development workload)*

---

## 🚀 How to Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/nopCommerce-local.git
   cd nopCommerce-local
Restore and build

bash
Copy code
dotnet restore .\src\Presentation\Nop.Web\Nop.Web.csproj
dotnet build .\src\Presentation\Nop.Web\Nop.Web.csproj
Run the application

bash
Copy code
cd .\src\Presentation\Nop.Web
dotnet run
Open in browser

arduino
Copy code
http://localhost:59580
The nopCommerce installation page will appear.

Complete installation

Choose SQL Server (LocalDB) or your own SQL instance.

Tick Create database if it does not exist.

Set admin email and password.

Click Install and wait until the site restarts.

Access Admin Panel

bash
Copy code
http://localhost:59580/admin
Log in with the credentials you created during installation.
