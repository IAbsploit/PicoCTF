# CTF Challenge Write-Up: Cookies

## **Challenge Overview**

* **Category**: Web 
* **Difficulty**: Easy *this is the only easy one*
* **Description**:
  This challenge was faily simple. The idea is to input different names until you get a flag. There is a place holder for a cookie name to start off with called "snickerdoodle". This then returns a successful ouput. Any input that is not expected will generate a red signal.

---

## **Steps to Solve**

### **Step 1: Recon**

* **Description**:
  Exploring the app I noticed after a you provide a successful cookie name to the web app, there is a certain value that changes called "name" inside the cookie field. 
  I changed the numbers and noticed that based on the number you give, it returns a different cookie name. 

* **web app**:
  ![image](https://github.com/user-attachments/assets/1b4c1ea5-425b-428b-a4dc-5c2ad9e02813)

  ![Screenshot of Initial Exploration](path_to_screenshot_1)
---

### **Step 2: Exploitation**

* **Description**:
  Based on the info found above, I decided to use BurpSuites's Intruder to change the number value up from 1 all the way to 20. 

* **BURP**:
  ![Screenshot of Exploitation](path_to_screenshot_2)
  ![image](https://github.com/user-attachments/assets/429f9a3b-3d03-4ee3-8d2f-801be0c7fd70)

---

### **Step 3: Flag Extraction**
I found that number 18 had an odd length field compared to the others. Once I opened it, I found the flag.
![image](https://github.com/user-attachments/assets/255145bf-47d0-4701-ad0c-abdc0a226b10)


---

* **Flag**: `picoCTF{****}`

---
