
---

### 🔹 **Level 14: User-Friendly Menu Script (`level14.md`)**

```markdown
# Level 14: User-Friendly Menu Script

## Objective:
Create a basic user menu for system actions.

## Script:
```bash
#!/bin/bash

echo "Choose an option:"
echo "1. Check disk space"
echo "2. Show system uptime"
echo "3. List users"

read -rp "Enter your choice [1-3]: " choice

case $choice in
    1) df -h ;;
    2) uptime ;;
    3) cut -d: -f1 /etc/passwd ;;
    *) echo "Invalid option" ;;
esac

