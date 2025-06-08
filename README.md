<img src="https://github.com/Hydra1536/Hack01/blob/main/matrix-code-animation-gif-free-animated-background.gif" alt="GitHub Banner" width="100%" />

<h1 align="center">Hi 👋, I'm MD Rezaul Karim</h1>

🎓 Final Year **CSE Student** at **BRAC University**  
🔍 **OSINT Specialist** | 📚 **Researcher** | 💻 **MERN, Laravel & Kotlin Developer** | 🛡️ **Penetration Testing Enthusiast**

---

## 💼 Current Roles

- 🧪 Conducting **Thesis Research** on *Mobile Security & Real-time Privacy Control*
- 🛡️ Practicing **Penetration Testing** & **Ethical Hacking**
- 📱 Developing mobile apps using **Kotlin**
- 💡 Contributing to academic and usability testing projects
- 🧠 Exploring **HCI** and privacy-aware app design

---

## 💻 Tech Stack

### 👨‍💻 Languages
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=yellow)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=""&logoColor=white)
![Java](https://img.shields.io/badge/Java-F7DF1E?style=for-the-badge&logo=java&logoColor=black)
![Assembly](https://img.shields.io/badge/Assembly-3776AB?style=for-the-badge&logo=assembly&logoColor=red)

### 🌐 Web & Mobile
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android_Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white)

### 🗃️ Databases
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00758F?style=for-the-badge&logo=mysql&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

### 🛡️ Cybersecurity Tools `Nmap` •acunetix • `Google Dorking` • `Recon-ng
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6600?style=for-the-badge&logo=burpsuite&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-3A3A3A?style=for-the-badge&logo=metasploit&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-557C94?style=for-the-badge&logo=nmap&logoColor=white)
![Acunetix](https://img.shields.io/badge/Acunetix-557C94?style=for-the-badge&logo=acunetix&logoColor=white)
![Google Dorking](https://img.shields.io/badge/Google_Dorking-557C94?style=for-the-badge&logo=googledorking&logoColor=white)
![Recon Ng](https://img.shields.io/badge/Recon_Ng-557C94?style=for-the-badge&logo=reconng&logoColor=white)


### 🧪 Tools & Research
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)

---

## 🔬 Research Interests

- 🔐 Mobile Privacy & Real-Time Alerts  
- 🧠 HCI & Usability Engineering  
- 🛡️ Security Awareness & Behavioral Research  
- 🌐 OSINT & Ethical Hacking  
- 🧩 Gamified Cybersecurity Education

---

## 📫 Let's Connect

- 🔗 [LinkedIn](https://www.linkedin.com/in/md-rezaul-karim-2423a621a/)
- 📧 Email: *reza15361382@gmail.com*

---

> “I aim to build secure, intelligent systems that protect users and promote digital trust.”

---

### 🐍 GitHub Activity Snake

<picture>
  name: GitHub Snake Game

on:
  # Schedule the workflow to run daily at midnight UTC
  schedule:
    - cron: "0 0 * * *"
  # Allow manual triggering of the workflow
  workflow_dispatch:
  # Trigger the workflow on pushes to the main branch
  push:
    branches:
      - main
jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      # Step 1: Checkout the repository
      - name: Checkout Repository
        uses: actions/checkout@v3
      # Step 2: Generate the snake animations
      - name: Generate GitHub Contributions Snake Animations
        uses: Platane/snk@v3
        with:
          # GitHub username to generate the animation for
          github_user_name: ${{ github.repository_owner }}
          # Define the output files and their configurations
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
      # Step 3: Deploy the generated files to the 'output' branch
      - name: Deploy to Output Branch
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
          publish_branch: output
          # Optionally, you can set a custom commit message
          commit_message: "Update snake animation [skip ci]"</picture>
