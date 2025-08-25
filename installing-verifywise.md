---
description: 'Complete installation guide with quick-start and comprehensive options'
---

# 💾 Installing VerifyWise

VerifyWise offers flexible installation options to suit different environments and use cases. Choose the method that best fits your needs.

## 🚀 Quick Start (5 minutes)

Perfect for trying VerifyWise quickly or demo purposes.

### Prerequisites
- Docker and Docker Compose installed
- 4GB+ available RAM
- Internet connection

### Installation Steps

1. **Create and navigate to installation directory:**
```bash
mkdir verifywise && cd verifywise
```

2. **Download installation files:**
```bash
wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/docker-compose.yml
wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/.env.prod
wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/install.sh
```

3. **Make installer executable and run:**
```bash
chmod +x install.sh
./install.sh
```

4. **Access VerifyWise:**
- Open your browser to: `http://localhost:3000`
- Default login: Create an account through the registration page

> **Screenshot Location:** *Dashboard welcome screen after successful login*

---

## 🏗️ Comprehensive Installation

For production deployments, development, or customized setups.

### System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| CPU | 2 cores | 4+ cores |
| RAM | 4GB | 8GB+ |
| Storage | 10GB | 50GB+ |
| OS | Linux/macOS/Windows | Ubuntu 20.04+ |

### Prerequisites Installation

#### Install Node.js and npm
```bash
# Ubuntu/Debian
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# macOS (using Homebrew)
brew install node

# Windows
# Download from https://nodejs.org/
```

#### Install Docker
```bash
# Ubuntu/Debian
sudo apt-get update
sudo apt-get install docker.io docker-compose
sudo usermod -aG docker $USER

# macOS
brew install docker docker-compose

# Windows
# Download Docker Desktop from https://docker.com/
```

### Installation Methods

## Method 1: Docker Production Setup (Recommended)

**Best for:** Production deployments, easy maintenance

1. **Create project directory:**
```bash
mkdir verifywise-production
cd verifywise-production
```

2. **Download production files:**
```bash
wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/docker-compose.prod.yml
wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/.env.prod
```

3. **Configure environment:**
```bash
cp .env.prod .env
nano .env  # Edit configuration as needed
```

4. **Start services:**
```bash
docker-compose -f docker-compose.prod.yml --env-file .env up -d
```

5. **Verify installation:**
```bash
docker ps  # Should show running containers
curl http://localhost:3000  # Should return HTML
```

## Method 2: Development Setup

**Best for:** Development, customization, contributing

1. **Clone repository:**
```bash
git clone https://github.com/bluewave-labs/verifywise.git
cd verifywise
```

2. **Set up environment:**
```bash
cp .env.dev .env
```

3. **Install client dependencies:**
```bash
cd Clients
npm install
cd ..
```

4. **Install server dependencies:**
```bash
cd Servers
npm install
cd ..
```

5. **Start database:**
```bash
docker run -d \
  --name verifywise-postgres \
  -p 5432:5432 \
  -e POSTGRES_PASSWORD=your_password \
  -e POSTGRES_DB=verifywise \
  postgres:16
```

6. **Start development servers:**
```bash
# Terminal 1 - Backend
cd Servers
npm run watch

# Terminal 2 - Frontend
cd Clients
npm run dev
```

7. **Access development environment:**
- Frontend: `http://localhost:5173`
- Backend API: `http://localhost:3000/api`

## Method 3: Manual Installation

**Best for:** Custom server setups, advanced configurations

### Database Setup
1. **Install PostgreSQL:**
```bash
sudo apt-get install postgresql postgresql-contrib
sudo systemctl start postgresql
sudo systemctl enable postgresql
```

2. **Create database:**
```bash
sudo -u postgres psql
CREATE DATABASE verifywise;
CREATE USER verifywise_user WITH PASSWORD 'secure_password';
GRANT ALL PRIVILEGES ON DATABASE verifywise TO verifywise_user;
\q
```

### Application Setup
1. **Clone and build:**
```bash
git clone https://github.com/bluewave-labs/verifywise.git
cd verifywise
```

2. **Configure environment:**
```bash
cp .env.example .env
# Edit .env with your database credentials
```

3. **Build and start:**
```bash
npm run build
npm run start
```

---

## 🔧 Post-Installation Setup

### Initial Configuration

1. **Access the application:**
   - Navigate to your VerifyWise URL (e.g., `http://localhost:3000`)
   
2. **Create administrator account:**
   - Click "Register" or "Sign Up"
   - Fill in administrator details
   - Verify email if configured

3. **Configure organization settings:**
   - Go to Settings → Organization
   - Set organization name, logo, and preferences

4. **Set up first project:**
   - Navigate to Dashboard
   - Click "Create New Project"
   - Follow the project setup wizard

### Essential Settings

- **User Management:** Configure roles and permissions
- **Security:** Enable 2FA, set password policies
- **Integrations:** Connect external tools if needed
- **Backup:** Configure automated backups

---

## ✅ Verification Checklist

After installation, verify these components work correctly:

- [ ] Can access login page
- [ ] Can create user account
- [ ] Dashboard loads properly
- [ ] Can create a new project
- [ ] Can navigate to all main sections
- [ ] Database connection is stable
- [ ] File uploads work (if applicable)

---

## 🔒 Security Considerations

### Production Security Checklist
- [ ] Change default passwords
- [ ] Enable HTTPS/SSL
- [ ] Configure firewall rules
- [ ] Set up regular backups
- [ ] Enable access logging
- [ ] Configure session timeouts
- [ ] Review user permissions

### Environment Variables Security
```bash
# Never commit these to version control
DB_PASSWORD=your_secure_password
JWT_SECRET=your_jwt_secret_key
API_ENCRYPTION_KEY=your_encryption_key
```

---

## 🆘 Troubleshooting Common Issues

### Port Conflicts
```bash
# Check what's using port 3000
lsof -i :3000
# Kill process if needed
sudo kill -9 <PID>
```

### Database Connection Issues
```bash
# Test database connection
pg_isready -h localhost -p 5432 -d verifywise
# Check PostgreSQL logs
sudo tail -f /var/log/postgresql/postgresql-*.log
```

### Docker Issues
```bash
# Restart Docker services
sudo systemctl restart docker
# View container logs
docker logs <container_name>
# Clean up Docker resources
docker system prune -a
```

### Permission Issues
```bash
# Fix file permissions
sudo chown -R $USER:$USER /path/to/verifywise
chmod -R 755 /path/to/verifywise
```

---

## 🔄 Updates and Maintenance

### Updating VerifyWise
```bash
# Docker installation
docker-compose pull
docker-compose up -d

# Development installation
git pull origin main
npm install  # In both Clients and Servers directories
npm run build
```

### Backup Procedures
```bash
# Database backup
pg_dump -h localhost -U verifywise_user verifywise > backup.sql

# File backup
tar -czf verifywise_backup.tar.gz /path/to/verifywise/data
```

---

## 📞 Getting Help

If you encounter issues during installation:

1. **Check logs:** Review application and system logs for errors
2. **Community:** Visit our GitHub Issues page
3. **Documentation:** Refer to specific component documentation
4. **Support:** Contact support team for production issues

**Next Steps:** Once installed, proceed to [Dashboard Overview](dashboard-overview.md) to start using VerifyWise.