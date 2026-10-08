## Install Node.js

**Download**: [nodejs.org](https://nodejs.org/)  
Pilih **LTS** (Long Term Support).

**macOS/Windows**: Download installer, install  
**Linux**: Via package manager
```bash
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
```

**Test**:
```bash
node --version  # v18.x.x atau v20.x.x
npm --version   # 9.x.x atau 10.x.x
```

**npm** = Node Package Manager (install library JavaScript).

**First package**:
```bash
npm install -g nodemon  # Tool auto-restart server
```

**Done!** Lu udah punya semua tools developer.
