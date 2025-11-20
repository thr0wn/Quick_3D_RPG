## RPG Prototype

### Fix permission issue on Ubuntu
Issue: https://github.com/electron/electron/issues/42510
Solution:
The solution is to lift the restrictions that Ubuntu 24.04 implements in the AppImages.
```bash
sudo sysctl -w kernel.apparmor_restrict_unprivileged_userns=0
```
for deactivate restrictions
```bash
sudo sysctl -w kernel.apparmor_restrict_unprivileged_userns=1
```
for activate restrictions
