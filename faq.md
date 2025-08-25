---
description: 'Frequently asked questions about VerifyWise AI governance platform'
---

# ❓ Frequently Asked Questions

Find quick answers to the most common questions about VerifyWise. Can't find what you're looking for? Check our [Troubleshooting Guide](troubleshooting.md) or [contact support](getting-support.md).

## 🚀 Getting Started

### What is VerifyWise?
VerifyWise is an open-source AI governance platform that helps organizations manage AI systems responsibly. It provides tools for compliance tracking, risk assessment, vendor management, and regulatory adherence across frameworks like EU AI Act and ISO 42001.

### Who should use VerifyWise?
- **AI/ML teams** developing AI systems
- **Compliance officers** ensuring regulatory adherence
- **Risk managers** assessing AI-related risks
- **Legal teams** managing AI governance
- **Organizations** of any size implementing AI

### Is VerifyWise free to use?
Yes, VerifyWise is open-source and free to use. You can self-host it on your own infrastructure or use managed hosting services.

### How long does setup take?
- **Quick start**: 5-10 minutes with Docker
- **Production setup**: 30-60 minutes
- **Full organization onboarding**: 2-4 hours

> **Screenshot Location:** *VerifyWise dashboard showing the main navigation and project overview*

---

## 🏗️ Installation & Setup

### What are the system requirements?
**Minimum:**
- 2 CPU cores, 4GB RAM, 10GB storage
- Docker and Docker Compose
- Modern web browser

**Recommended for production:**
- 4+ CPU cores, 8GB+ RAM, 50GB+ storage
- PostgreSQL database
- SSL certificate for HTTPS

### Can I install VerifyWise on Windows?
Yes, VerifyWise works on Windows, macOS, and Linux. Docker Desktop is recommended for Windows installations.

### Do I need technical expertise to set up VerifyWise?
Basic Docker knowledge is helpful but not required. Our installation guide provides step-by-step instructions for both technical and non-technical users.

### Can I migrate data from other governance tools?
Yes, VerifyWise provides data import capabilities. Contact support for assistance with specific migration scenarios.

---

## 👥 User Management & Access

### How many users can I have?
There's no limit on the number of users in the open-source version. User capacity depends on your server resources.

### What user roles are available?
- **Admin**: Full system access and configuration
- **Editor**: Create and modify projects, assessments, risks
- **Reviewer**: Review and approve compliance items
- **Auditor**: Read-only access for compliance audits

### How do I invite new users?
Go to Settings → Team Management → "Invite User". Enter their email address and select appropriate role and permissions.

### Can users have different permissions per project?
Yes, permissions can be configured at both the organization and project levels, allowing fine-grained access control.

### What if a user forgets their password?
Users can reset passwords using the "Forgot Password" link on the login page, or admins can reset passwords in user management.

---

## 📊 Projects & Assessment

### How many projects can I create?
There's no limit on the number of projects. Performance depends on your server resources and database capacity.

### What compliance frameworks are supported?
- **EU AI Act** (complete implementation)
- **ISO 42001** (AI management systems)
- **ISO 27001** (information security)
- **Custom frameworks** (configurable)

### Can I create custom assessment questions?
Yes, you can customize existing frameworks and create entirely custom assessment criteria to match your organization's needs.

### How long does a typical assessment take?
- **Initial assessment**: 4-8 hours per project
- **Ongoing maintenance**: 1-2 hours per month
- **Time varies** based on project complexity and team size

### Can multiple people work on the same project?
Yes, projects support team collaboration with role-based permissions, activity tracking, and concurrent editing capabilities.

---

## ⚠️ Risk Management

### How does risk assessment work?
VerifyWise uses a structured approach combining impact and likelihood ratings to calculate risk levels, with customizable risk matrices and mitigation tracking.

### Can I import existing risk registers?
Yes, you can import risks from Excel/CSV files or integrate with other risk management tools via API.

### What risk categories are available?
Standard categories include:
- Privacy and data protection
- Bias and fairness
- Safety and security
- Transparency and explainability
- Human oversight
- Custom categories (configurable)

### How often should I update risk assessments?
We recommend:
- **Monthly reviews** for high-risk projects
- **Quarterly reviews** for medium-risk projects
- **Event-driven updates** when significant changes occur

---

## 👨‍💻 Vendor Management

### Why is vendor management important for AI governance?
Many AI systems rely on third-party services, APIs, or data. Vendor management ensures these external dependencies meet your governance standards.

### What vendor information should I track?
- Vendor contact details and contracts
- Services provided and data processed
- Security and compliance certifications
- Risk assessments and mitigation plans
- Performance monitoring and reviews

### Can I link vendors to multiple projects?
Yes, vendors can be associated with multiple projects, and their risk assessments can be shared across projects.

---

## 🔒 Security & Privacy

### Is my data secure in VerifyWise?
Yes, VerifyWise implements security best practices:
- Encrypted data transmission (HTTPS)
- Secure password hashing
- Role-based access control
- Audit logging
- Regular security updates

### Where is my data stored?
With self-hosted VerifyWise, your data stays on your infrastructure. You have complete control over data location and security.

### Is VerifyWise GDPR compliant?
Yes, VerifyWise is designed with privacy by design principles and supports GDPR compliance requirements including data portability and deletion.

### Can I backup my data?
Yes, regular database backups are recommended. VerifyWise provides backup scripts and restoration procedures.

---

## 🔌 Integrations & API

### Does VerifyWise have an API?
Yes, VerifyWise provides a comprehensive REST API for all platform features. See our [API Reference](api-reference.md) for details.

### What systems can I integrate with?
Common integrations include:
- **Identity providers** (LDAP, Active Directory, SAML)
- **Project management tools** (Jira, Asana)
- **Documentation systems** (Confluence, SharePoint)
- **Risk management platforms**
- **CI/CD pipelines**

### Can I automate workflows?
Yes, using the API and webhooks, you can automate:
- Project creation and updates
- Assessment submissions
- Risk monitoring and alerts
- Compliance reporting

---

## 📊 Reporting & Analytics

### What reports can I generate?
- **Compliance reports** by framework
- **Risk assessment summaries**
- **Project progress reports**
- **Audit trail reports**
- **Custom reports** via API

### Can I customize report formats?
Yes, you can customize report templates, include/exclude sections, and export in multiple formats (PDF, Excel, CSV).

### How often are reports updated?
Reports reflect real-time data. Scheduled automated reports can be configured via API integration.

---

## 🔧 Technical Questions

### What browsers are supported?
- Chrome (recommended)
- Firefox
- Safari
- Edge
- Mobile browsers (responsive design)

### Can I use VerifyWise on mobile devices?
Yes, VerifyWise has a responsive design that works on tablets and smartphones, though some complex workflows are better suited for desktop use.

### What if I encounter performance issues?
Check our [Troubleshooting Guide](troubleshooting.md) for performance optimization tips, or consider:
- Increasing server resources
- Database optimization
- Network connectivity improvements

### How do I update VerifyWise?
Updates depend on your installation method:
- **Docker**: Pull latest images and restart
- **Manual installation**: Follow upgrade instructions
- Always backup before updating

---

## 💰 Licensing & Support

### What license is VerifyWise released under?
VerifyWise is released under an open-source license, allowing free use, modification, and distribution.

### Is commercial support available?
Yes, professional support, training, and consulting services are available for organizations requiring additional assistance.

### Can I contribute to VerifyWise development?
Absolutely! VerifyWise welcomes community contributions. Check our GitHub repository for contribution guidelines.

### How do I get help if I'm stuck?
1. Check this FAQ and [documentation](README.md)
2. Search [GitHub Issues](https://github.com/bluewave-labs/verifywise/issues)
3. Create a new issue with details
4. Join community discussions
5. Contact support for urgent issues

---

## 🔄 Migration & Data

### Can I export my data?
Yes, VerifyWise supports data export in multiple formats:
- Database dumps
- JSON export via API
- CSV/Excel exports for reports
- Individual file downloads

### How do I migrate between VerifyWise instances?
Use database backup/restore procedures or API-based data migration scripts. Contact support for assistance with large migrations.

### What happens if I want to switch from VerifyWise?
Your data remains accessible through exports. VerifyWise avoids vendor lock-in by using standard formats and providing comprehensive export capabilities.

---

## 🚨 Emergency & Troubleshooting

### What if VerifyWise won't start?
1. Check Docker containers are running
2. Verify database connectivity
3. Check logs for error messages
4. Ensure ports aren't blocked
5. See [Troubleshooting Guide](troubleshooting.md)

### I lost access to my admin account. What do I do?
If you have database access, you can reset the admin password directly in the database or create a new admin user using the database scripts.

### Can I recover deleted projects?
Deleted projects may be recoverable from database backups if available. Regular backups are essential for data recovery.

### The system is slow. How can I improve performance?
- Check available system resources (CPU, RAM)
- Optimize database queries
- Clear browser cache
- Restart VerifyWise services
- Review server capacity

---

## 🎓 Training & Best Practices

### Is training available?
Yes, we provide:
- Self-paced documentation and guides
- Video tutorials (planned)
- Professional training services
- Community workshops

### What are the best practices for using VerifyWise?
- Start with a pilot project
- Define clear roles and responsibilities
- Regular team training and updates
- Consistent documentation practices
- Regular reviews and improvements

### How should I structure my organization in VerifyWise?
- Create projects per AI system/initiative
- Use clear naming conventions
- Assign dedicated project owners
- Regular cross-project reviews
- Document decision-making processes

---

## 📞 Still Need Help?

If you can't find the answer to your question:

1. **Search our documentation** - Use the search function to find specific topics
2. **Check GitHub Issues** - Someone might have asked the same question
3. **Create a new issue** - Provide detailed information about your question
4. **Join the community** - Connect with other VerifyWise users
5. **Contact support** - For urgent or complex issues

**Related Documentation:**
- [Installation Guide](installing-verifywise.md) - Detailed setup instructions
- [Troubleshooting Guide](troubleshooting.md) - Common issues and solutions  
- [API Reference](api-reference.md) - Technical integration details
- [Getting Support](getting-support.md) - Support options and contact methods