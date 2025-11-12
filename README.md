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

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/nopCommerce-local.git
cd nopCommerce-local
```

---

### 2️⃣ Restore and build the project
```bash
dotnet restore .\src\Presentation\Nop.Web\Nop.Web.csproj
dotnet build .\src\Presentation\Nop.Web\Nop.Web.csproj
```

---

### 3️⃣ Run the application
```bash
cd .\src\Presentation\Nop.Web
dotnet run
```

You’ll see something like:
```
Now listening on: http://localhost:59580
Now listening on: https://localhost:59579
```

---

### 4️⃣ Open the site in your browser
Go to:
```
http://localhost:59580
```

You’ll see the nopCommerce installation page.

---

### 5️⃣ Complete installation
- **Database:** choose **SQL Server (LocalDB)** or your own SQL instance.  
- **Check:** “Create database if it does not exist”.  
- **Set:** Admin email and password.  
- Click **Install** and wait until the site restarts.

---

### 6️⃣ Access the Admin Panel
Once the installation finishes, open:
```
http://localhost:59580/admin
```

Then log in using the **admin email and password** you just created.

---

## 🧪 For Automation Testers
Use the running base URL (e.g. `http://localhost:59580`) as your `baseUrl` in your automation framework.

---

## 🧰 Notes
- Stop the server anytime with **Ctrl + C**.  
- To run again later:
  ```bash
  cd src/Presentation/Nop.Web
  dotnet run
  ```
- Database and configuration are stored in your local SQL instance.
- This setup is mainly used for testing and integration with the automation project.
