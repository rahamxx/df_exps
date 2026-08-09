# Password Capturing Using Wireshark

> **Laboratory Experiment Report & Documentation**  
> *Demonstrating packet analysis and credential exposure over unencrypted HTTP connections.*

---

## ⚠️ Disclaimer & Notice

* **Educational Purpose Only:** Perform packet captures only on networks, devices, and applications for which you have explicit authorization.
* **Encrypted Protocols:** HTTPS/TLS is designed to encrypt transport layer communications, preventing credentials from appearing as readable HTTP form data.

---

## 📑 Objective

Demonstrate how packet analyzers (such as Wireshark) can capture and expose sensitive information (usernames, passwords) transmitted through an unencrypted HTTP connection within an authorized laboratory environment.

---

## 🛠️ Tools & Display Filters Used

### Tool
* **Wireshark:** Open-source network protocol analyzer.

### Useful Display Filters
| Filter | Description |
| :--- | :--- |
| `http` | Filters all Hypertext Transfer Protocol traffic |
| `http.request.method == "GET"` | Isolates HTTP GET requests |
| `http.request.method == "POST"` | Isolates HTTP POST requests (typically used for form submissions) |

---

## 🔄 Experiment Workflow

Start Capture ──► 2. Open Login Page ──► 3. Filter Traffic (http) ──► 4. Inspect GET Requests ──► 5. Inspect POST Requests ──► 6. Expand Form Data


---

## 📝 Step-by-Step Execution & Evidence

### Step 1: Start Wireshark Packet Capture

Start a live capture session on the active network interface (e.g., **Wi-Fi**). Network packets are collected continuously before, during, and after web interactions.

* **Target Interface:** `\Device\NPF_{B049A020-DB50-40FE-B845-853876C58588}` (Wi-Fi)
* **Protocols captured:** TCP, TLSv1.3, UDP, etc.

---

### Step 2: Access Insecure Login Page & Submit Credentials

Navigate to the unencrypted test web application and submit form credentials.

* **Target URL:** `http://testasp.vulnweb.com/Login.asp?RetURL=/Templatize.asp?item=html/about.html`
* **Test Application:** Acunetix Acuforum (Deliberately vulnerable test site)
* **Submitted Fields:**
  * **Username:** `raham`
  * **Password:** `12345678`

---

### Step 3: Filter Captured Traffic for HTTP

To isolate HTTP traffic from background network noise, enter the display filter `http` in the Wireshark filter bar.

* **Filter Bar Query:** `http`
* **Observed Traffic:** GET and POST requests flowing between the client IP (`2409:40f4:10fd:fa82:...`) and the target server IP (`64:ff9b::2cee:1df4`).

---

### Step 4: Inspect HTTP GET Requests

Filter for GET requests using `http.request.method == "GET"`.

* **Observation:** GET requests retrieve resources from the server but generally do not contain sensitive payload data like password form submissions.
* **Filter:** `http.request.method == "GET"`

---

### Step 5 & 6: Locate and Inspect HTTP POST Request

Filter for HTTP POST requests using `http.request.method == "POST"` to find form submission packets.

* **Selected Packet:** Packet `34811`
* **Method:** `POST /Login.asp?RetURL=/Templatize.asp?item=html/about.html HTTP/1.1`
* **Content-Type:** `application/x-www-form-urlencoded`
* **Packet Length:** 869 bytes

---

### Step 7: Expand HTML Form URL Encoded Payload

In the Packet Details pane of Wireshark, expand the **HTML Form URL Encoded** field:

```text
HTML Form URL Encoded: application/x-www-form-urlencoded
    ├── Form item: "tfUName" = "raham"
    └── Form item: "tfUPass" = "12345678"
Exposed Credentials Extracted:
tfUName: raham

tfUPass: 12345678
