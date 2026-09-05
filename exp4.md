# 📧 Email Header Analysis and Email Spoofing Detection Using MHA

## 📌 Experiment No. 4

### 🎯 Aim

To analyze email headers and detect possible email spoofing using **MHA (Mail Header Analyzer)**.

---

## 📖 Description

Email header analysis is used to examine the metadata of an email. It helps identify the sender, recipient, email servers, IP addresses, authentication results, and possible signs of email spoofing.

---

## 🛠️ Procedure

### 1️⃣ Access the Email Header
<img width="1897" height="975" alt="Screenshot 2026-09-05 102157" src="https://github.com/user-attachments/assets/5da2fec3-bef1-4e07-a6ee-91160428fb83" />

#### Gmail

1. Open the email.
2. Click the **three dots (More)** in the upper-right corner.
3. Select **Show original**.
<img width="1798" height="895" alt="Screenshot 2026-09-05 103126" src="https://github.com/user-attachments/assets/3b7fdb45-08b5-4aa5-84fd-2ce1be2659f8" />

#### Outlook

1. Open the email.
2. Click **File**.
3. Select **Properties**.
4. Find the **Internet headers** section.

#### Yahoo

1. Open the email.
2. Click the **three dots (More)**.
3. Select **View raw message**.

---

### 2️⃣ Copy the Email Header

Once the email header is displayed, copy all the text.

The header contains metadata about the journey of the email from the sender to the recipient.
<img width="1908" height="638" alt="Screenshot 2026-09-05 103216" src="https://github.com/user-attachments/assets/66e4957c-48bd-480c-89e1-c93935214861" />

---

## 🔍 3️⃣ Identify Key Header Fields

| Header Field    | Description                                          |
| --------------- | ---------------------------------------------------- |
| **From**        | Sender's email address                               |
| **To**          | Recipient's email address                            |
| **Date**        | Date and time the email was sent                     |
| **Subject**     | Subject line of the email                            |
| **Return-Path** | Return address if the email bounces                  |
| **Received**    | List of servers through which the email passed       |
| **Message-ID**  | Unique identifier of the email                       |
| **SPF**         | Checks whether the sender's IP is authorized         |
| **DKIM**        | Verifies the authenticity and integrity of the email |
| **DMARC**       | Uses SPF and DKIM for email authentication           |

---

## 🌐 4️⃣ Analyze the `Received` Fields

The `Received` fields show the path taken by an email from the sender to the recipient.

The fields are generally listed in **reverse order**, from the last server to the first server.

Each `Received` entry may contain:

* Sending server hostname
* Sending server IP address
* Receiving server hostname
* Receiving server IP address
* Date and time of transmission

<img width="1501" height="771" alt="Screenshot 2026-09-05 111750" src="https://github.com/user-attachments/assets/c8c1b9ea-a28d-48dd-9c7e-736642653345" />

---

## 🔎 5️⃣ Check IP Addresses and Hostnames

Use tools such as **WHOIS** or online IP lookup services to investigate IP addresses found in the `Received` fields.

Check whether:

* The IP address belongs to the expected mail server.
* The hostname matches the sending server.
* The IP address appears suspicious.
* The location of the IP address is unexpected.
<img width="1573" height="867" alt="Screenshot 2026-09-05 111014" src="https://github.com/user-attachments/assets/b76bb385-e3a2-46f3-8109-2c5bdbd30211" />

---

## 🔐 6️⃣ Examine SPF, DKIM, and DMARC Results

### SPF – Sender Policy Framework

SPF checks whether the sender's IP address is authorized to send emails for a particular domain.

* ✅ **Pass:** The IP address is authorized.
* ❌ **Fail:** The IP address is not authorized and may indicate spoofing.

### DKIM – DomainKeys Identified Mail

DKIM verifies whether the email content has been altered during transmission.

* ✅ **Pass:** The email has not been tampered with.
* ❌ **Fail:** The email content may have been altered.

### DMARC

DMARC uses SPF and DKIM policies to authenticate an email.

* ✅ **Pass:** Indicates alignment with SPF/DKIM policies.
* ❌ **Fail:** May indicate spoofing or tampering.
<img width="703" height="117" alt="Screenshot 2026-09-05 111917" src="https://github.com/user-attachments/assets/9bf1f227-e216-44ce-b093-f990c4280bf5" />

---

## 🆔 7️⃣ Analyze the `Message-ID`

The `Message-ID` is a unique identifier for an email.

It usually contains the domain of the sending server.

Check whether the domain in the `Message-ID` matches the sender's domain.

A mismatch may indicate possible email spoofing.

---

## ⚠️ 8️⃣ Look for Anomalies

### 📧 Email Domain Mismatch

Check whether the domain in:

```text
From
Return-Path
Message-ID
```

matches the expected sender domain.

### 🌍 Strange IP Addresses

Be cautious of IP addresses that:

* Do not belong to the expected mail server.
* Come from unexpected locations.
* Have suspicious ownership information.

### ⏰ Suspicious Timestamps

Check the timestamps in the `Received` fields.

Significant time differences may indicate:

* Delays
* Rerouting
* Suspicious email activity

---

## 🛠️ 9️⃣ Use Online Analysis Tools

Online email header analysis tools can automatically parse and analyze email headers.

Examples include:

* MXToolbox
* Google G Suite Toolbox

These tools can help identify:

* IP addresses
* Mail servers
* Authentication results
* Routing information
<img width="1831" height="877" alt="Screenshot 2026-09-05 105533" src="https://github.com/user-attachments/assets/bb573a1c-da35-4c60-ab00-dd880ad007f7" />
<img width="1757" height="777" alt="Screenshot 2026-09-05 105200" src="https://github.com/user-attachments/assets/87de9edb-d9f8-4daf-bcbf-d2fa863eab3c" />

---

## 📝 🔟 Document and Report Findings

Document all findings during the investigation.

If phishing or email spoofing is detected:

* Record the suspicious information.
* Preserve the email header.
* Report the suspicious email to the IT department.
* Report the email to the email service provider.

---

# 🧪 Example Email Header Analysis

## Sample Header

```text
Received: from mail.example.com (mail.example.com [192.0.2.1])
 by mail.receiver.com with ESMTP id u29si8604336pjs.40.2023.08.10.07.00.16;
 Thu, 10 Aug 2023 07:00:16 -0700 (PDT)

Received: by mail.example.com with SMTP id a1mr1243772ywh.51;
 Thu, 10 Aug 2023 07:00:15 -0700 (PDT)

Message-ID: <CA+7eu=4pSeXgQ@mail.example.com>
```

## Analysis

### 1. Check the IP Address

Look up:

```text
192.0.2.1
```

Verify whether it is associated with:

```text
mail.example.com
```

### 2. Verify SPF and DKIM

Check whether the sending server is authorized to send emails for the specified domain.

### 3. Compare Timestamps

Ensure that the timestamps are in chronological order and do not show unusual delays.

---

# 📋 Email Spoofing Detection Checklist

* [ ] Check the `From` address.
* [ ] Check the `Return-Path`.
* [ ] Analyze the `Received` fields.
* [ ] Investigate IP addresses.
* [ ] Verify SPF authentication.
* [ ] Verify DKIM authentication.
* [ ] Verify DMARC authentication.
* [ ] Check the `Message-ID`.
* [ ] Compare email domains.
* [ ] Check timestamps.
* [ ] Document suspicious findings.

---

# 🔄 Workflow

```text
Access Email
      │
      ▼
View Email Header
      │
      ▼
Copy Complete Header
      │
      ▼
Identify Important Fields
      │
      ▼
Analyze Received Fields
      │
      ▼
Check IP Addresses & Hostnames
      │
      ▼
Verify SPF / DKIM / DMARC
      │
      ▼
Analyze Message-ID
      │
      ▼
Look for Anomalies
      │
      ▼
Document Findings
      │
      ▼
Detect Possible Email Spoofing
```

---

# 🧰 Tools Used

* **MHA (Mail Header Analyzer)**
* **WHOIS**
* **Online IP Lookup Tools**
* **MXToolbox**
* **Google G Suite Toolbox**

---

# 📊 Key Concepts

| Concept            | Description                                    |
| ------------------ | ---------------------------------------------- |
| **Email Header**   | Metadata containing information about an email |
| **Received**       | Shows the route taken by an email              |
| **SPF**            | Validates the sending IP address               |
| **DKIM**           | Verifies email integrity                       |
| **DMARC**          | Uses SPF and DKIM authentication               |
| **Message-ID**     | Unique identifier of an email                  |
| **Email Spoofing** | Forging an email sender identity               |

---

# 🧪 Result

The email header was successfully analyzed using the **MHA (Mail Header Analyzer)** approach.

Important fields such as `Received`, IP addresses, hostnames, `Message-ID`, SPF, DKIM, and DMARC were examined to identify anomalies and detect possible email spoofing.

---

# 🏁 Conclusion

Email header analysis is an important technique in digital forensics and cybersecurity. By examining routing information, sender details, IP addresses, authentication results, and anomalies, investigators can identify suspicious emails and possible email spoofing.
