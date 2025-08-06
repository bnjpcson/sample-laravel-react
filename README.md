# 🛠️ Project Setup Guide

This guide will help you install and run the application on your local machine.

---

## 📦 Installation Steps

### 1. Clone the Repository

Start by cloning the project to your local machine:

```bash
git clone https://github.com/your-username/your-repository.git
```

### 2. Install Dependencies

Navigate into the project folder and run the following commands:

```bash
composer install
npm install
```

These commands will install all necessary PHP and Node.js packages.

### 3. Set Up the Database

🗃️ Create a MySQL Database

Use your preferred tool (e.g., phpMyAdmin, MySQL Workbench, or terminal) to create a new MySQL database.

Make note of the database name for the next step.

### 4. Configure Environment Variables

🔧 Set up the .env file

Duplicate the `.env.example` file and rename the copy to `.env`:

```bash
cp .env.example .env
```

Open the .env file and update the following database configuration lines:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=root
DB_PASSWORD=
```

### 5. Run Migrations

Now, run the migration files to create the necessary database tables:

```bash
php artisan migrate
```

### 6. Start the Application

Finally, start the development server with:

```bash
composer run dev
```