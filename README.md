# 🛡️ Linux SOC Defense Lab

## 🇹🇷 Proje Açıklaması
Bu proje, Linux sistemler üzerinde gerçekleştirilen siber saldırıların tespit edilmesi, analiz edilmesi ve savunma mekanizmalarının uygulanmasını içeren pratik bir SOC (Security Operations Center) laboratuvarıdır.

Amaç; gerçek dünya senaryolarına yakın bir ortamda:
- Saldırıları gözlemlemek
- Log analizi yapmak
- Savunma mekanizmaları geliştirmek
- Sistem güvenliğini artırmak

---

## 🇬🇧 Project Description
This project is a hands-on Security Operations Center (SOC) lab focused on detecting, analyzing, and defending against cyber attacks on Linux systems.

The goal is to simulate real-world scenarios to:
- Observe attacks
- Perform log analysis
- Implement defensive mechanisms
- Improve system security posture

---

## 🎯 Lab Senaryoları | Lab Scenarios

### 🔐 1. SSH Brute Force Attack
- SSH servisine brute force saldırısı simülasyonu
- Failed login denemelerinin incelenmesi

📸  
SSH Attack

---

### 📊 2. Log Analysis
- /var/log/auth.log analizi
- Şüpheli IP ve aktivitelerin tespiti

📸  
Log Analysis

---

### 🛡️ 3. Fail2Ban Defense
- Fail2Ban kurulumu ve yapılandırması
- Otomatik IP banlama mekanizması

📸  
Fail2Ban

---

### 🌐 4. Nginx Status Monitoring
- Web server durum kontrolü
- Servis sağlık analizi

📸  
Nginx

---

### 🌍 5. Web Access Logs
- Web erişim loglarının analizi
- Trafik ve istek incelemesi

📸  
Web Logs

---

## 🧰 Kullanılan Teknolojiler | Technologies Used

- Linux (Ubuntu)
- OpenSSH
- Fail2Ban
- Nginx
- System Logs (auth.log, access.log)
- Git & GitHub

---

## ⚙️ Kurulum | Setup

### 🇹🇷
bash sudo apt update && sudo apt upgrade -y sudo apt install openssh-server nginx fail2ban -y 

### 🇬🇧
bash sudo apt update && sudo apt upgrade -y sudo apt install openssh-server nginx fail2ban -y 

---

## 🔍 Öğrenilenler | Key Learnings

### 🇹🇷
- Brute force saldırıları nasıl çalışır
- Log analizi nasıl yapılır
- Fail2Ban ile sistem nasıl korunur
- Web server logları nasıl incelenir

### 🇬🇧
- How brute force attacks work
- How to analyze logs
- How to secure systems using Fail2Ban
- How to analyze web server logs

---

## 📁 Proje Yapısı | Project Structure
bash linux-soc-defense-lab/ │ ├── screenshots/ │   ├── 01-ssh-bruteforce-attack.png │   ├── 02-log-analysis.png │   ├── 03-fail2ban-defense.png │   ├── 04-nginx-status.png │   └── 05-web-access.png │ └── README.md 

---

---

## 🔥 Attack Evidence | Saldırı Kanıtı

bash Failed password for root from 192.168.1.100 port 22 ssh2 Failed password for admin from 192.168.1.100 port 22 ssh2 Failed password for invalid user test from 192.168.1.100 port 22 ssh2 

---

## 🔒 Fail2Ban Response | Fail2Ban Tepkisi

bash Status for the jail: sshd |- Filter |  |- Currently failed: 5 |  |- Total failed: 25 |  `- Journal matches: _SYSTEMD_UNIT=sshd.service `- Actions    |- Currently banned: 1    |- Total banned: 1    `- Banned IP list: 192.168.1.100 

---

## ⚡ Attack Flow | Saldırı Akışı

Attacker IP → SSH brute force → Log detection → Fail2Ban trigger → IP banned

---

## 🧠 Detection Logic | Tespit Mantığı

### 🇬🇧 English
- Multiple failed SSH login attempts detected via /var/log/auth.log
- Repeated authentication failures from a single IP address
- Threshold exceeded based on Fail2Ban configuration
- Automatic banning mechanism triggered

### 🇹🇷 Türkçe
- /var/log/auth.log üzerinden çoklu başarısız SSH giriş denemeleri tespit edildi
- Tek bir IP adresinden tekrar eden başarısız girişler gözlemlendi
- Fail2Ban yapılandırmasına göre eşik değer aşıldı
- Otomatik engelleme mekanizması tetiklendi

---

## 🛡️ Security Outcome | Güvenlik Sonucu

### 🇬🇧 English
- Brute force attack successfully identified
- Malicious IP automatically blocked
- Unauthorized access attempts prevented
- System integrity maintained

### 🇹🇷 Türkçe
- Brute force saldırısı başarıyla tespit edildi
- Zararlı IP otomatik olarak engellendi
- Yetkisiz erişim girişimleri önlendi
- Sistem bütünlüğü korundu

---

## 🎯 Project Value | Proje Değeri

### 🇬🇧 English
This project demonstrates hands-on experience in:
- Real-world attack detection
- Log analysis and threat identification
- Automated defense mechanisms
- SOC-oriented security monitoring approach

### 🇹🇷 Türkçe
Bu proje aşağıdaki konularda pratik deneyim sunmaktadır:
- Gerçek dünya saldırı tespiti
- Log analizi ve tehdit belirleme
- Otomatik savunma mekanizmaları
- SOC odaklı güvenlik izleme yaklaşımı


## 🚀 Amaç | Purpose

### 🇹🇷
Bu proje, siber güvenlik alanında kendini geliştirmek isteyenler için pratik bir referans ve portföy çalışmasıdır.

### 🇬🇧
This project serves as a practical reference and portfolio piece for those looking to improve their cybersecurity skills.

---

## 👤 Author

Murat Karateke

---

## ⭐ Not
Bu proje, siber güvenlik öğrenme sürecinin bir parçası olarak hazırlanmıştır ve gerçek dünya senaryolarını simüle ettim.
