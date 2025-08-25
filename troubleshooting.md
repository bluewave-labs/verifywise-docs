---
description: 'Comprehensive troubleshooting guide for common VerifyWise issues'
---

# 🛠️ Troubleshooting Guide

This guide helps you resolve common issues when using VerifyWise. Find solutions quickly with our organized troubleshooting sections.

## 🚀 Quick Problem Solver

### Most Common Issues
1. **Can't log in** → [Login Issues](#login-and-authentication-issues)
2. **Dashboard not loading** → [Performance Issues](#performance-issues)
3. **Can't create projects** → [Project Creation Issues](#project-creation-issues)
4. **Files won't upload** → [File Upload Issues](#file-upload-issues)
5. **Pages are slow** → [Performance Issues](#performance-issues)

### Emergency Checklist ✅
- [ ] Check internet connection
- [ ] Try refreshing the page (Ctrl+F5 or Cmd+Shift+R)
- [ ] Clear browser cache and cookies
- [ ] Try a different browser
- [ ] Check if the issue affects other users

> **Screenshot Location:** *Browser developer console showing common error messages*

---

## 🔐 Login and Authentication Issues

### Issue: Cannot Log In with Correct Credentials

**Symptoms:**
- "Invalid credentials" error with correct username/password
- Login form resets after submission
- Redirect loops after login attempt

**Solutions:**

1. **Clear Browser Data**
   ```bash
   # Chrome: Settings → Privacy → Clear browsing data
   # Firefox: Settings → Privacy → Clear Data
   # Safari: Develop → Empty Caches
   ```

2. **Check Account Status**
   - Ensure account hasn't been deactivated
   - Check if password has expired
   - Verify account hasn't been locked

3. **Browser-Specific Fixes**
   - Disable browser extensions temporarily
   - Enable JavaScript and cookies
   - Try incognito/private browsing mode

### Issue: Session Expired Messages

**Symptoms:**
- Frequent "Session expired" notifications
- Automatic logouts during work
- Loss of unsaved work

**Solutions:**

1. **Check Session Settings**
   - Contact admin to review session timeout settings
   - Ensure system clock is accurate

2. **Browser Configuration**
   - Allow cookies for VerifyWise domain
   - Check if cookie duration is being limited

### Issue: Two-Factor Authentication Problems

**Symptoms:**
- 2FA codes not working
- QR code not scanning
- Backup codes not accepted

**Solutions:**

1. **Time Synchronization**
   ```bash
   # Check system time is accurate
   # For mobile authenticator apps, sync time
   ```

2. **Backup Recovery**
   - Use backup recovery codes
   - Contact administrator for 2FA reset

---

## ⚡ Performance Issues

### Issue: Slow Page Loading

**Symptoms:**
- Pages take more than 10 seconds to load
- Timeout errors
- Blank or partially loaded pages

**Diagnostic Steps:**

1. **Check Network Connection**
   ```bash
   # Test connection speed
   ping docs.verifywise.ai
   
   # Check DNS resolution
   nslookup verifywise.ai
   ```

2. **Browser Performance**
   - Close unnecessary browser tabs
   - Clear browser cache
   - Disable resource-heavy extensions

3. **System Resources**
   - Check available RAM and CPU
   - Close other applications
   - Restart browser if necessary

### Issue: Dashboard Not Loading

**Symptoms:**
- White screen after login
- Dashboard widgets not appearing
- JavaScript errors in console

**Solutions:**

1. **Browser Console Check**
   - Press F12 to open developer tools
   - Look for red errors in Console tab
   - Take screenshot of errors for support

2. **Progressive Loading**
   - Wait 30 seconds for full load
   - Try refreshing specific sections
   - Use browser back/forward buttons

### Issue: High Memory Usage

**Symptoms:**
- Browser becomes unresponsive
- System slowdown
- Out of memory errors

**Solutions:**

1. **Browser Optimization**
   - Limit open tabs to 5 or fewer
   - Use browser task manager to identify heavy tabs
   - Restart browser regularly

2. **System Optimization**
   - Close unnecessary applications
   - Check available system memory
   - Consider upgrading RAM if consistently low

---

## 📁 Project Creation Issues

### Issue: Cannot Create New Projects

**Symptoms:**
- "Create Project" button not responding
- Project creation form not submitting
- Permission denied errors

**Solutions:**

1. **Permission Verification**
   - Check with admin about project creation permissions
   - Verify your user role allows project creation
   - Confirm organization limits haven't been reached

2. **Form Validation Issues**
   - Ensure all required fields are completed
   - Check for special characters in project name
   - Verify date formats match expected format

### Issue: Project Settings Not Saving

**Symptoms:**
- Settings revert after saving
- "Save failed" error messages
- Changes don't persist between sessions

**Solutions:**

1. **Network Connectivity**
   - Check stable internet connection
   - Try saving in smaller increments
   - Wait for confirmation before navigating away

2. **Data Validation**
   - Check all required fields are complete
   - Verify data formats (dates, emails, etc.)
   - Remove special characters if causing issues

---

## 📤 File Upload Issues

### Issue: Files Won't Upload

**Symptoms:**
- Upload progress bar freezes
- "Upload failed" error messages
- Files appear but aren't processing

**Solutions:**

1. **File Size and Format**
   ```
   Maximum file size: 50MB per file
   Supported formats: PDF, DOC, DOCX, XLS, XLSX, PNG, JPG
   ```

2. **Network Stability**
   - Ensure stable internet connection
   - Try uploading smaller files first
   - Use wired connection if on WiFi

3. **Browser Configuration**
   - Enable JavaScript and cookies
   - Temporarily disable antivirus/firewall
   - Try different browser

### Issue: Upload Progress Stuck

**Symptoms:**
- Progress bar stops at specific percentage
- Long wait times with no completion
- Browser tab becomes unresponsive

**Solutions:**

1. **File Optimization**
   - Compress large files before upload
   - Split large documents into smaller parts
   - Remove embedded images if not necessary

2. **Upload Strategy**
   - Upload files one at a time
   - Avoid uploading during peak hours
   - Use smaller batches for multiple files

---

## 🔍 Data and Content Issues

### Issue: Missing Project Data

**Symptoms:**
- Projects showing as empty
- Historical data not visible
- Recent changes not appearing

**Solutions:**

1. **Data Synchronization**
   - Wait 5 minutes and refresh
   - Check if other team members see same issue
   - Log out and log back in

2. **Browser Issues**
   - Clear browser cache and cookies
   - Try incognito/private mode
   - Use different browser to verify

### Issue: Incorrect Dashboard Metrics

**Symptoms:**
- Wrong numbers in dashboard widgets
- Outdated progress indicators
- Inconsistent data across sections

**Solutions:**

1. **Data Refresh**
   - Use manual refresh button if available
   - Wait for automatic sync (usually 15 minutes)
   - Check if issue affects all projects or specific ones

2. **Calculation Verification**
   - Manually verify a few calculations
   - Check if recent changes haven't been processed
   - Report discrepancies to support with specifics

---

## 🌐 Browser-Specific Issues

### Chrome Issues
- **Memory Problems**: Enable memory saver mode
- **Extension Conflicts**: Disable ad blockers and security extensions
- **Update Required**: Keep Chrome updated to latest version

### Firefox Issues
- **Privacy Settings**: Adjust strict privacy settings
- **Cache Problems**: Clear storage completely
- **Add-on Interference**: Disable all add-ons temporarily

### Safari Issues
- **Cookie Blocking**: Enable cross-site tracking
- **Cache Issues**: Develop menu → Empty Caches
- **Security Settings**: Allow JavaScript from VerifyWise domain

### Edge Issues
- **Compatibility Mode**: Ensure not running in IE compatibility
- **Privacy Settings**: Allow necessary cookies and scripts
- **Extension Issues**: Check if extensions cause conflicts

---

## 📱 Mobile and Tablet Issues

### Issue: Mobile Interface Problems

**Symptoms:**
- UI elements overlapping
- Touch interactions not working
- Horizontal scrolling issues

**Solutions:**

1. **Browser Optimization**
   - Use Chrome or Safari on mobile
   - Enable desktop mode if necessary
   - Clear mobile browser cache

2. **Display Settings**
   - Rotate to landscape mode for complex views
   - Zoom out to see full interface
   - Use responsive design mode

### Issue: Touch and Navigation Problems

**Solutions:**
- Double-tap instead of single tap for some actions
- Use long press for context menus
- Swipe gently to avoid accidental navigation

---

## 🔧 Advanced Troubleshooting

### Developer Console Debugging

1. **Open Browser Console** (F12)
2. **Check Console Tab** for JavaScript errors
3. **Network Tab** for failed requests
4. **Application Tab** for storage issues

### Common Error Messages and Solutions

| Error Message | Likely Cause | Solution |
|---------------|--------------|----------|
| "Network Error" | Internet connectivity | Check connection, retry |
| "Permission Denied" | User access level | Contact administrator |
| "Session Expired" | Authentication timeout | Log out and log back in |
| "Server Error 500" | Backend issue | Wait and retry, contact support |
| "Not Found 404" | Broken link/URL | Check URL, try navigation menu |

### Performance Monitoring

1. **Page Load Speed**
   - Use browser developer tools
   - Check Network tab for slow requests
   - Monitor resource usage

2. **Memory Usage**
   - Chrome: More tools → Task manager
   - Check memory usage per tab
   - Close heavy tabs if needed

---

## 📞 When to Contact Support

### Gather This Information Before Contacting Support:

**System Information:**
- Operating system and version
- Browser type and version
- VerifyWise URL being used
- Time when issue occurred

**Issue Details:**
- Exact steps to reproduce the problem
- Error messages (screenshots helpful)
- How often the issue occurs
- Whether it affects other users

**Impact Assessment:**
- How many users affected
- Business impact level
- Urgency of resolution needed

### Support Contact Methods:
- **GitHub Issues**: For bugs and feature requests
- **Documentation**: Check other sections of this guide
- **Administrator**: Contact your organization's VerifyWise admin
- **Community**: Join user community discussions

### Creating Effective Support Requests:

1. **Clear Subject Line**: "Project creation fails with error 500"
2. **Step-by-Step**: Exact reproduction steps
3. **Screenshots**: Visual evidence of the issue
4. **Impact**: How it affects your work
5. **Attempted Solutions**: What you've already tried

---

## ✅ Prevention and Best Practices

### Regular Maintenance:
- Clear browser cache weekly
- Keep browser updated
- Regular password updates
- Monitor system resources

### Optimal Usage Patterns:
- Save work frequently
- Limit concurrent browser tabs
- Use recommended browsers
- Regular logout/login for long sessions

### Data Safety:
- Regular project backups
- Document important configurations
- Keep evidence files organized
- Maintain audit trails

**Related Documentation:**
- [Installation Guide](installing-verifywise.md) for setup issues
- [Settings Guide](settings.md) for configuration problems
- [Project Guide](getting-started-with-projects.md) for project-specific issues