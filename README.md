# Gate Pass Management System (GPMS)

A comprehensive web-based application designed to streamline and automate the process of managing visitor access to facilities. The system provides an intuitive administrative interface for creating, tracking, and managing gate passes with real-time analytics and reporting capabilities.

## 🚀 Features

### Core Functionality
- 🔐 **Secure Authentication**: Admin login system with session management
- 🎫 **Pass Management**: Create, edit, view, and manage visitor passes
- 📊 **Real-time Dashboard**: Live statistics and analytics
- 👤 **Visitor Registration**: Comprehensive visitor information capture
- 📈 **Status Tracking**: Monitor pass status and validity
- 🖨️ **Print Functionality**: Generate printable pass documents

### Technical Features
- 📱 **Responsive Design**: Mobile-friendly interface using Bootstrap 5
- 🗄️ **Database Management**: MySQL-based data storage and retrieval
- ✅ **Form Validation**: Client-side and server-side validation
- 🔒 **Security**: SQL injection prevention and secure session handling
- 🎨 **Modern UI**: Professional design with Font Awesome icons
- 🌐 **Server**: Apache (XAMPP)

## 📁 Project Structure

```
getpass/
├── index.php              # Login page and authentication
├── dashboard.php          # Main dashboard with statistics
├── add-pass.php          # Pass creation form
├── manage-passes.php     # List and manage all passes
├── edit-pass-detail.php  # Edit existing pass information
├── view-pass-detail.php  # Detailed pass view
├── logout.php            # Session termination
├── db.php               # Database connection configuration
├── database/
│   └── getpassdb.sql    # Database schema and sample data
└── includes/
    ├── header.php       # Common header with styling
    ├── sidebar.php      # Navigation sidebar
    └── footer.php       # Common footer with scripts
```

## 🚀 Installation

### Prerequisites
- XAMPP (Apache + MySQL + PHP)
- PHP 7.2.1 or higher
- MySQL/MariaDB database
- Modern web browser with JavaScript enabled

### Setup Instructions

1. **Clone/Download the Project**
   ```bash
   # Place the project files in your XAMPP htdocs directory
   # Example: C:\xampp\htdocs\getpass\
   ```

2. **Database Setup**
   - Start XAMPP and ensure Apache and MySQL services are running
   - Open phpMyAdmin (http://localhost/phpmyadmin)
   - Create a new database named `getpassdb`
   - Import the database schema from `database/getpassdb.sql`

3. **Configuration**
   - Open `db.php` and verify database connection settings:
     ```php
     define('DB_SERVER', 'localhost');
     define('DB_USERNAME', 'root');
     define('DB_PASSWORD', '');
     define('DB_NAME', 'getpassdb');
     ```

4. **Access the Application**
   - Open your web browser
   - Navigate to: `http://localhost/getpass/`
   - Login with default credentials:
     - **Username**: admin
     - **Password**: admin

## 📊 System Features

### Dashboard Analytics
- 📊 **Total Passes**: Complete count of all passes in the system
- 📅 **Daily Passes**: Number of passes created today
- 📈 **Weekly Passes**: Passes generated in the last 7 days

### Pass Management
- 👤 **Visitor Information**: Name, contact, email, identity details
- 🏷️ **Pass Categories**: Different visitor types (Visitor, Contractor, etc.)
- 🆔 **Identity Verification**: Support for multiple ID types (Aadhar, PAN, etc.)
- 📅 **Date Management**: From and to date selection for pass validity
- 📊 **Status Tracking**: Monitor pass approval and validity status

### Administrative Functions
- ⚡ **CRUD Operations**: Create, Read, Update, Delete passes
- 🔍 **Search & Filter**: Find specific passes quickly
- 🖨️ **Print Passes**: Generate printable pass documents
- 📤 **Data Export**: View comprehensive pass details

## 🔒 Security Features

- 🛡️ **SQL Injection Prevention**: Input sanitization using `mysqli_real_escape_string()`
- 🔐 **Session Management**: Secure session handling with automatic logout
- 🚫 **Access Control**: Admin-only access to system functions
- 🔑 **Password Protection**: MD5 hashed passwords (consider upgrading to stronger hashing for production)

## 🎨 User Interface

- 📱 **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- 🎨 **Bootstrap Framework**: Modern, clean, and professional appearance
- 🧭 **Intuitive Navigation**: Easy-to-use sidebar menu with active page highlighting
- ✅ **Form Validation**: Real-time validation with user-friendly error messages
- 🖨️ **Print-Ready Output**: Clean formatting for pass document printing

## 📋 Database Schema

### Admin Table
- `id` (Primary Key)
- `username` (VARCHAR)
- `password` (VARCHAR - MD5 hashed)
- `updation_date` (TIMESTAMP)

### Passes Table
- `id` (Primary Key)
- `pass_number` (VARCHAR - Auto-generated)
- `full_name` (VARCHAR)
- `contact_number` (BIGINT)
- `email` (VARCHAR)
- `identity_type` (VARCHAR)
- `identity_card_no` (VARCHAR)
- `category` (VARCHAR)
- `from_date` (DATE)
- `to_date` (DATE)
- `reason` (MEDIUMTEXT)
- `pass_creation_date` (TIMESTAMP)
- `status` (VARCHAR - Default: 'Pending')

## 🔧 Configuration

### Database Connection
Edit `db.php` to match your database settings:
```php
define('DB_SERVER', 'localhost');
define('DB_USERNAME', 'your_username');
define('DB_PASSWORD', 'your_password');
define('DB_NAME', 'getpassdb');
```

### Default Admin Credentials
- **Username**: admin
- **Password**: admin

**⚠️ Important**: Change the default password after first login for security.

## 🚀 Usage Guide

### Creating a New Pass
1. Login to the system
2. Click "Add Pass" in the sidebar
3. Fill in visitor details:
   - Full name, contact number, email
   - Identity document type and number
   - Pass category and validity dates
   - Reason for visit
4. Click "Create Pass"

### Managing Passes
1. Navigate to "Manage Passes" to view all passes
2. Use "View" to see detailed pass information
3. Use "Edit" to modify pass details
4. Use "Print" to generate a printable pass document

### Dashboard Overview
- View real-time statistics on the main dashboard
- Monitor daily and weekly pass generation trends
- Access quick navigation to all system functions

## 🔍 Troubleshooting

### Common Issues

**🔌 Database Connection Error**
- Verify XAMPP services are running
- Check database credentials in `db.php`
- Ensure database `getpassdb` exists

**🔐 Login Issues**
- Confirm admin credentials are correct
- Check if sessions are enabled in PHP
- Verify file permissions

**🖨️ Print Functionality Not Working**
- Ensure JavaScript is enabled in browser
- Check browser print settings
- Verify no popup blockers are active

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

1. 🍴 Fork the repository
2. 🌿 Create a feature branch
3. ✏️ Make your changes
4. ✅ Test thoroughly
5. 📤 Submit a pull request

## 📞 Support

For support and questions:
- 🐛 Create an issue in the repository
- 🔍 Check the troubleshooting section above
- 📖 Review the code comments for implementation details

## 🔄 Version History

- **v1.0.0**: Initial release with core functionality
  - 🎫 Basic pass management system
  - 🔐 Admin authentication
  - 📊 Dashboard analytics
  - ⚡ CRUD operations

---

**⚠️ Note**: This system is designed for educational and organizational use. For production deployment, consider implementing additional security measures such as stronger password hashing, HTTPS, and regular security audits. 
