# My Devops Practicum
# 🐳 Part 1: Installing Docker on Ubuntu

## 📦 Step 1: Remove old versions (if any)

```bash
sudo apt remove docker docker-engine docker.io containerd runc
```

🔹 This command removes any old versions of Docker that might be accidentally installed.

---

## 📦 Step 2: Install required dependencies

```bash
sudo apt update
sudo apt install ca-certificates curl gnupg lsb-release -y
```

🔹 These are necessary packages to add Docker's official repository.

---

## 📦 Step 3: Add Docker’s GPG key (for security)

```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

🔹 This is like a “digital signature” — it tells Ubuntu the repository is trusted and from Docker.

---

## 📦 Step 4: Add the official Docker repository

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

🔹 This tells the system to download Docker packages from the official source.

---

## 📦 Step 5: Install Docker Engine

```bash
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```

🔹 This is the main step — installing Docker Engine and its tools.

---

## 📦 Step 6: Verify Docker installation

```bash
sudo docker version
sudo docker info
```

---

## 🧑‍💻 Step 7 (Optional): Allow running Docker without `sudo`

```bash
sudo usermod -aG docker $USER
```

Then log out and log back in to apply the group change.

---

✅ You're now ready to use Docker on your Ubuntu system!

