# 🖥 How to Connect Your GitHub Account to a Fresh Windows Install
<img width="611" height="379" alt="image" src="https://github.com/user-attachments/assets/062e9e5b-52f6-401f-9e71-d082656c1d16" />

## 1️⃣ Download and Install Git
- Download latest version: [git-scm.com/download/win](https://git-scm.com/download/win)
  
  <img width="678" height="258" alt="1" src="https://github.com/user-attachments/assets/4188a3ff-4d58-45fc-8c4e-6e4a845a6ed7" />
  

- Run the installer and click **Next** until you see **"Use Vim" as default editor**.
  
  <img width="628" height="487" alt="2" src="https://github.com/user-attachments/assets/22e301fa-8076-4bb7-912a-39320fccc2de" />
  
  > ❌ No! Unless you enjoy pain.  
  ✅ Choose Notepad or any editor you have installed, you can always change later.  

- Continue clicking **Next, Next, Next** until it starts installing.
  
<img width="327" height="216" alt="image" src="https://github.com/user-attachments/assets/70be90b6-ff58-464f-8e16-ea0abe52afd8" />

---

## 2️⃣ Finish Installation
- When complete, check **"Launch Git Bash"** and click **Finish**.
  
<img width="492" height="418" alt="3 - installation complete" src="https://github.com/user-attachments/assets/8c387e29-f321-428f-965e-b0ac1c0fa3ba" />

---

## 3️⃣Git Bash opens: 
<img width="600" height="770" alt="image" src="https://github.com/user-attachments/assets/cdd547a3-6029-4713-a41c-f10e4565e7bf" />

---

## 4️⃣ Set Your Git Identity
In Git Bash, set your username and email to match your GitHub account:

```git config --global user.name "YourGitHubUsername"```
```git config --global user.email "your@email.com"```

ℹ️ Use the same email that’s set as your primary email in GitHub.

<img width="651" height="147" alt="5 - config GitHub" src="https://github.com/user-attachments/assets/0bc5dc0b-a0e3-4669-8ba5-4be946675357" />

---


## 5️⃣ Generate a New SSH Key 

*In Git Bash, run:
```ssh-keygen -t ed25519 -C "your@email.com"```

<img width="440" height="57" alt="image" src="https://github.com/user-attachments/assets/0d5a1b19-78a0-4c66-aaff-3e0125aafe3a" />

---

## 6️⃣ Press Enter to accept the default save location.

**Optionally set a passphrase** (can be empty – just press Enter)


---

## 7️⃣ Git will generate a keyfingerprint and an image 


---

## 8️⃣ Add Your SSH Key to the SSH Agent 🗝  
  This tells Windows/Git to remember your SSH key in memory so you don’t have to type the passphrase every time you push or pull:


<img width="351" height="137" alt="6 - ssh key (watch out for spaces)" src="https://github.com/user-attachments/assets/d3a28c57-f112-4b0a-bc6c-565b0e35e2da" />


⚠️**WATCH OUT FOR SPACES** when you type in the command


<img width="262" height="281" alt="image" src="https://github.com/user-attachments/assets/14f1ac69-dde1-4ba8-a2dd-1c4d785829a1" />


---

## 9️⃣  Add Your SSH Key to GitHub
**Copy the SSH key** (in Git Bash, type this):  
    
```bash
cat ~/.ssh/id_ed25519.pub
```
  
This command will print your **public SSH key** in Git Bash.  

**Then:**  
1. Go to **GitHub → Settings → SSH and GPG keys**  
2. Click **New SSH key**
   <img width="1599" height="261" alt="7 - new SSH key" src="https://github.com/user-attachments/assets/428f1f59-48ac-48a8-a6cc-05a670ceeb5c" />
   
3. Give it a title (e.g., `"My Windows PC"`)  
4. Paste the key from Git Bash  
5. Click **Add SSH key**
     

---

## 🔟 Test the Connection

<img width="580" height="580" alt="image" src="https://github.com/user-attachments/assets/65c78d81-7606-4996-aed9-90f6179dbe12" />

   In bash, type 
   ```bash
   ssh -T git@github.com
```
   
**The message will be :**
**"The authenticity of host 'github.com (140.82.121.3)' can't be established.**
**This key is not known by any other names.**
**Are you sure you want to continue connecting (yes/no/[fingerprint])?"** 

## Here’s what it means in plain English:

"Permanently added 'github.com'..." → Your computer now trusts GitHub’s fingerprint, so it won’t ask you again.
"Hi MihaelaChicu! You've successfully authenticated..." → GitHub has confirmed your SSH key matches your account. You’re officially connected. ✅

<img width="577" height="39" alt="9 - Test the connection and succeed" src="https://github.com/user-attachments/assets/378801b3-2e0c-4d55-8251-f3956b1a1791" />

"...but GitHub does not provide shell access." → Normal message. GitHub doesn’t give you a remote terminal, only Git repo access.



**Don't panic** 

<img width="563" height="413" alt="image" src="https://github.com/user-attachments/assets/c4c743a1-9d9f-4537-92e4-d477d76945df" />

This is the first time you’re connecting to GitHub from this computer. Should I trust this server’s fingerprint?”
It’s a security handshake to make sure you’re actually talking to GitHub and not some fake server.

**Type - yes**

then you will see "You've successfully authenticated" message

<img width="666" height="168" alt="8 - victory" src="https://github.com/user-attachments/assets/77c7fa69-0cf5-4ffd-b7bc-92ace433ffbc" />



---



