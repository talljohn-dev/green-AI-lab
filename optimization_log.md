# Windows Optimization Log — HP Notebook Node

**Date:** October 2025  
**System:** HP Notebook X7T50UA#ABA  
**OS:** Windows 10 Home 64-bit  
**Processor:** Intel Core i3-6100U @ 2.3 GHz  
**RAM:** 6 GB usable  

---

## Actions Taken

| Step | Action | Tool | Result |
|------|---------|------|--------|
| 1 | Removed startup bloatware | Task Manager | Boot time reduced |
| 2 | Ran `sfc /scannow` | PowerShell (Admin) | Fixed 1 corrupted file |
| 3 | Ran `chkdsk` | PowerShell (Admin) | No errors found |
| 4 | Disabled visual effects | System Properties | Less lag |
| 5 | Set power plan to “Performance” | Control Panel | Better responsiveness |

---

## Results

| Metric | Before | After | Improvement |
|---------|---------|--------|-------------|
| Boot Time | 2 min 10 s | 1 min 02 s | -52 % |
| Free Disk Space | 795 GB | 855 GB | + 60 GB |
| CPU Idle Load | 22 % | 8 % | -14 % |
| RAM Usage at Idle | 3.2 GB | 2.0 GB | -1.2 GB |

---

**Next Step:** Install Ubuntu Server dual-boot and convert this node to your first Green AI Lab server.