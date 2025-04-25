
# Sudo and System Administration Notes

## What is `sudo`?

- `sudo` = **Super User DO**
- Grants temporary **root privileges**
  - Safer than logging in to the root account directly

## How to Add User to `sudo` Group?

### On Debian/Ubuntu:
```bash
usermod -aG sudo <username>
```

### On RHEL/CentOS:
```bash
usermod -aG wheel <username>
```

## Edit `sudoers` File

```bash
sudo visudo
```

- This opens `/etc/sudoers`
- **Important:** Always check the syntax before saving to prevent lockouts.

## Log Files for Tracking `sudo` Activity

- **Ubuntu/Debian:**
  ```
  /var/log/auth.log
  ```

- **RHEL/CentOS:**
  ```
  /var/log/secure
  ```

---

## File Permissions

- **Creating a New Directory with Permissions:**
  ```
  mkdir <dir_name> && chmod 755 <dir_name>
  ```
  - `755` = rwxr-xr-x (Owner: read/write/execute, Group: read/execute, Others: read/execute)

---

## Package Management System (To be continued...)
