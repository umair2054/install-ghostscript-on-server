# Installing Ghostscript 10.03.1 Without Sudo

This guide will help you install Ghostscript (gs10.03.1) locally on your server or instance without needing `sudo` privileges. The installation will be done in your home directory.

## Steps to Install Ghostscript Locally

### 1. Download Ghostscript Source
Download the source code for Ghostscript version 10.03.1 using `wget`:

```bash
wget https://github.com/ArtifexSoftware/ghostpdl-downloads/releases/download/gs10031/ghostscript-10.03.1.tar.gz
```

### 2. Extract the Source
```bash
tar -zxvf ghostscript-10.03.1.tar.gz
```

### 3. Configure the Build
```bash
cd ghostscript-10.03.1
./configure --prefix=$HOME/ghostscript
```

### 4. Compile Ghostscript
```bash
make
```

### 5. Install Ghostscript Locally
```bash
make install
```

### 6. Update Your PATH
```bash
export PATH=$HOME/ghostscript/bin:$PATH
```

### 7. Verify Installation
```bash
gs --version
```
You should see the output like this 10.03.1

### Ghostscript Installation Completed!
