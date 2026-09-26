# 🔐 Password Recovery & Hash Analysis: John the Ripper (JTR) & Networkwalks Tools

## 📌 Project Overview

This project demonstrates the process of **auditing, extracting, and recovering passwords from password-protected PDF documents** using offline and web-based hash-cracking techniques.

By leveraging the **John the Ripper (JTR) Application** and **NETWORKWALKS Tools**, this lab demonstrates how cryptographic information is extracted from protected documents, converted into a format that password-recovery tools can process, and subjected to dictionary/wordlist-based attacks to recover credentials.

The project involved three separate password-protected PDF documents:

* 🔒 **My Locked PDF 1**
* 🔒 **My Locked PDF 2**
* 🔒 **My Locked PDF 3**

Each document had a different password, and all three passwords were successfully recovered and verified.

---

# 🎯 Objectives

The main objectives of this project were to:

### 🔹 Understand Hash Extraction

Learn how password-protected PDF files use encryption parameters and how this information can be represented in hash formats.

### 🔹 Offline Hash Cracking

Execute dictionary and wordlist-based attacks using the **John the Ripper application** against extracted PDF hashes.

### 🔹 Online Hash Cracking

Utilize browser-based utilities provided by **NETWORKWALKS Tools** for lightweight online password-recovery workflows.

### 🔹 Credential Verification

Validate recovered passwords by successfully unlocking and accessing the protected original PDF documents.

### 🔹 Security Assessment

Evaluate password strength and understand why short, common, or predictable passwords can be vulnerable to password-recovery utilities.

---

# ⚠️ Security & Ethical Use Disclaimer

🛡️ The techniques, software, and tools documented in this repository are intended for:

* 🎓 Educational purposes
* 🔐 Authorized security testing
* 📁 Personal credential recovery
* 🧪 Cybersecurity training laboratories

> ⚠️ Executing password attacks against systems or files **without explicit permission from the owner** is illegal and violates cybersecurity ethics.

All password-recovery activities documented in this project were performed within an authorized cybersecurity training/laboratory environment.

---

# 📖 Introduction to Password Cracking

Password cracking is the process of recovering passwords from stored cryptographic hashes or encrypted containers.

Modern applications generally do not store passwords directly. Depending on the application or file format, passwords may be represented through hashes, encryption parameters, or keys derived from passwords.

When attempting to access an encrypted document such as a protected PDF, an auditor cannot simply read the protected contents without the appropriate password.

Instead, the password-recovery process generally involves:

1. 🔍 Extracting the document's encryption parameters and hash structure.
2. 🧩 Passing the extracted information to a password-recovery engine such as John the Ripper.
3. 📚 Generating candidate passwords from a wordlist.
4. 🔄 Testing the candidates against the target password-protection information.
5. 🔑 Identifying a matching password.
6. 📄 Using the recovered password to verify access to the original protected document.

This project demonstrated this process using both **John the Ripper** and **NETWORKWALKS Tools**.

---

# 🛠️ Technical Execution & Methodology

## 💻 Method 1: Offline Attack via John the Ripper (JTR)

### 🔹 Step 1: Hash Extraction

The target password-protected PDF file was uploaded to an online hash-extraction utility to convert the PDF's password-protection information into a crackable hash string.

The resulting hash was exported and saved into a plain-text file for use with John the Ripper.

### 🧩 Hash Converter

The hash-extraction stage provided the information required by the JTR application to identify and process the protected PDF.

---

### 🔹 Step 2: Executing John the Ripper

The **John the Ripper (JTR) App** was launched.

The saved hash file was imported into the application interface.

The appropriate wordlist dictionary was selected, and the password-recovery attack was initiated.

The JTR application processed candidate passwords until a matching password was identified.

### 🔓 Cracked Password

The password was successfully recovered from the PDF hash.

The recovered password was then recorded and used during the verification stage.

---

### 🔹 Step 3: Verifying Document Access

The recovered plain-text password was copied from the JTR application.

The original protected PDF file was opened, the recovered password was entered, and the document was successfully unlocked.

### ✅ Verification Result

This confirmed that the password recovered from the hash corresponded to the password protecting the original PDF.

---

# 🌐 Method 2: Web-Based Attack via NETWORKWALKS Tools

## 🔹 Step 1: Generating the Hash via Hash Calculator

The **NETWORKWALKS Hash Calculator** was used to extract the password-protection hash from the encrypted PDF.

The target PDF was uploaded to the Hash Calculator.

The tool generated the corresponding hash string containing the PDF-specific information required by the password-cracking tool.

The complete hash string was then copied for use in the password-cracking stage.

### 🧮 Hash Calculator

The extracted hash was used as the input for the NETWORKWALKS Password Cracker.

---

## 🔹 Step 2: Cracking via NETWORKWALKS Password Cracker

The **NETWORKWALKS Password Cracker** interface was opened in a web browser.

The complete PDF hash string was pasted into the designated hash input field.

The attack was started, and the tool tested candidate passwords until a matching password was identified.

The interface displayed:

> 🎉 **PASSWORD CRACKED SUCCESSFULLY**

along with the recovered plain-text password.

---

## 🔹 Step 3: Document Decryption Verification

The recovered plain-text password was copied from the NETWORKWALKS interface.

The password was then applied to the original protected PDF.

Successful access to the document confirmed that the recovered credential was correct.

### ✅ PDF Decrypted Successfully

This provided an additional verification of the password-recovery results.

---

# 🔐 Three PDF Password Recovery Results

The project involved **three separate password-protected PDF documents**, with each document protected by a different password.

## 📄 My Locked PDF 1

The password-recovery process successfully identified the password as:

🔑 **`good-luck`**

The recovered password was used to unlock and verify the protected PDF.

✅ **Result: Successfully recovered and verified.**

---

## 📄 My Locked PDF 2

The password-recovery process successfully identified the password as:

🔑 **`password1`**

The recovered password was used to unlock and verify the protected PDF.

✅ **Result: Successfully recovered and verified.**

---

## 📄 My Locked PDF 3

The password-recovery process successfully identified the password as:

🔑 **`1qaz2wsx`**

The NETWORKWALKS interface confirmed the successful recovery with:

> 🎉 **PASSWORD CRACKED SUCCESSFULLY**

The recovered password was then used to verify access to the protected PDF.

✅ **Result: Successfully recovered and verified.**

---

# 📊 Password Recovery Summary

| 📄 Protected PDF | 🔑 Recovered Password | 📌 Status                |
| ---------------- | --------------------- | ------------------------ |
| My Locked PDF 1  | **`good-luck`**       | ✅ Successfully recovered |
| My Locked PDF 2  | **`password1`**       | ✅ Successfully recovered |
| My Locked PDF 3  | **`1qaz2wsx`**        | ✅ Successfully recovered |

### 🎯 Final Result

**All three protected PDF passwords were successfully recovered and verified.**

---

# 🏁 NETWORKWALKS Lab Results

After successfully completing the password-recovery exercises, the Networkwalks training environment displayed successful challenge/flag confirmations.

### 🚩 Flag 1

```text
nw{networkwalks_persistence_jtr_270521}
```

### 🚩 Flag 2

```text
nw{cybersecurity_flag_captured_2608}
```

### 🚩 Flag 3

```text
nw{networkwalks_flag_260821_1}
```

🏆 These flags provided confirmation of successful completion of the corresponding Networkwalks exercises.

---

# 🧠 What I Learned

## 🔍 Hash Structure Standardization

I identified how PDF password-protection information is structured and represented in a format that password-recovery tools such as John the Ripper can process.

I also learned that the hash format provides information that allows the cracking engine to determine how the protected document should be processed.

---

## 💻 Offline vs. Online Cracking Workflows

Offline cracking using dedicated applications such as **John the Ripper** allows password-recovery operations to be performed locally while providing flexibility with wordlists and attack configurations.

Online utilities such as **NETWORKWALKS Tools** provide a convenient browser-based workflow for extracting PDF hash information and performing password-recovery exercises.

---

## 🔐 Impact of Password Entropy

I observed firsthand how simple, common, or predictable passwords can be recovered using wordlist-based password attacks.

The three passwords recovered during the project were:

* 🔑 **`good-luck`**
* 🔑 **`password1`**
* 🔑 **`1qaz2wsx`**

These examples demonstrate why passwords should not be based on common words, common password combinations, or predictable keyboard patterns.

---

## ✅ Credential Verification

I also learned the importance of verifying a recovered password against the original protected document.

Finding a candidate password is not enough by itself. Successfully using that password to unlock the original PDF provides confirmation that the recovered credential is correct.

---

# 🐛 Issues Faced During the Project

## ⚠️ Hash Formatting Errors

Initially, I encountered issues where the copied hash string omitted structural information, preventing the JTR application from parsing the hash properly.

Ensuring that the complete PDF hash string was preserved resolved the issue.

---

## 📚 Wordlist Coverage Limits

Default or short wordlists did not always contain the required password during early test iterations.

Using an appropriate and sufficiently comprehensive wordlist allowed the password-recovery process to identify the matching password.

---

## 🌐 Browser Session Timeouts

During online password-recovery exercises with NETWORKWALKS Tools, larger wordlist lookups occasionally caused browser latency.

Using targeted hash sets and appropriate wordlists helped ensure smoother operation.

---

## 📂 Multiple Protected Documents

The project involved three separate PDF files, each protected by a different password.

Keeping the hashes, passwords, and verification results associated with the correct PDF was therefore important.

The final results were:

```text
📄 My Locked PDF 1 → good-luck
📄 My Locked PDF 2 → password1
📄 My Locked PDF 3 → 1qaz2wsx
```

---

# 🧰 Tools Used

### 🔨 John the Ripper (JTR) App

Offline application used for password recovery and hash cracking.

### 🔄 Online PDF Hash Extractor

Web utility used to parse protected PDF files and export password-recovery hash strings.

### 🧮 NETWORKWALKS Hash Calculator

Online tool used for extracting password-protection hash information from PDF documents.

### 🌐 NETWORKWALKS Password Cracker

Web-based password-recovery interface used to test candidate passwords against extracted PDF hashes.

### 📚 Wordlist Dictionary

Standard or custom wordlists used for generating password candidates during the recovery process.

### 📄 Protected PDF Documents

Three password-protected PDFs were used as the authorized targets for the exercise.

---

# 🛡️ Security Takeaway

This project demonstrates why password strength is an important part of information security.

The three passwords recovered during the exercise were:

| 📄 Document     | 🔐 Recovered Password |
| --------------- | --------------------- |
| My Locked PDF 1 | **`good-luck`**       |
| My Locked PDF 2 | **`password1`**       |
| My Locked PDF 3 | **`1qaz2wsx`**        |

The successful recovery of these passwords demonstrates that passwords containing common words, predictable combinations, or recognizable keyboard patterns can be vulnerable to dictionary and wordlist-based attacks.

For stronger protection, users should use:

* 🔒 Long and unique passwords
* 🎲 Unpredictable passphrases
* 🚫 No common words or keyboard patterns
* ♻️ No password reuse across accounts or files
* 🔑 A reputable password manager where appropriate

---

# 🎓 Conclusion

This project provided practical experience with **John the Ripper (JTR)** and **NETWORKWALKS Tools** for authorized PDF password recovery and hash analysis.

The project covered the complete workflow, including:

1. 📄 Preparing password-protected PDF files
2. 🔍 Extracting password-protection hash information
3. 🧩 Loading hashes into password-recovery tools
4. 📚 Performing wordlist-based password-recovery attacks
5. 🔑 Recovering the passwords
6. ✅ Verifying the recovered passwords against the original PDF documents
7. 🏁 Completing the associated Networkwalks lab challenges

Three separate protected PDF files were successfully recovered:

| 📄 File             | 🔑 Recovered Password |
| ------------------- | --------------------- |
| **My Locked PDF 1** | **`good-luck`**       |
| **My Locked PDF 2** | **`password1`**       |
| **My Locked PDF 3** | **`1qaz2wsx`**        |

🏆 The Networkwalks lab also confirmed successful completion through the captured flags.

This exercise strengthened my understanding of:

* 🔐 PDF password protection
* 🔍 Hash extraction
* 📚 Wordlist-based password recovery
* 💻 John the Ripper
* 🌐 Browser-based security tools
* ✅ Password verification
* 🛡️ Password security best practices

---

# 📸 Project Screenshots

<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/0311e358-4bec-405a-8c7c-b716f55e6e17" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/4306f474-3e08-4dab-a333-63f47a24c81a" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/fbb9aa68-dd63-4f9e-97d4-85b8fe89bfb9" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/1a5ca273-b424-4682-b8ab-1d1c95d65c31" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/3a06da48-be70-4dcf-adbf-79dfeaf9ca44" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/f0cd3efa-e009-417e-8d38-daab37e33c46" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/c6601aa0-ab78-40b3-bb65-c5958deaf797" />
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/b3b76554-7ed2-4984-bef6-9144261880f2" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/3f64e80a-036a-40b7-aded-b05ddc0ba15b" />

<img width="1241" height="1754" alt="My Locked PDF1_page-0001" src="https://github.com/user-attachments/assets/1a95d577-51ac-4e92-b02b-091c70ca537a" />
<img width="1241" height="1754" alt="My Locked PDF2_page-0001" src="https://github.com/user-attachments/assets/35f4ae07-dde6-4cd9-805b-5eb9db324f9c" />
<img width="1275" height="1650" alt="My Locked PDF3_page-0001" src="https://github.com/user-attachments/assets/c903ee2f-8c92-4d3f-a1a4-c83c5120421c" />



---

# 👨‍💻 Author

**Ismail Victor Elias**

🎓 **Cybersecurity Intern**