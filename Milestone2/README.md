# ⚡ FranchiseOps AI — Enterprise Multi-Agent Operations Platform

**FranchiseOps AI** is an end-to-end, multi-agent AI system designed for franchise network management, operational telemetry analysis, workforce retention modeling, and dynamic inventory control. Built on top of **Qwen-2.5-3B-Instruct (4-bit quantized)**, it integrates localized weather intelligence, multi-algorithm machine learning pipelines, and enterprise security controls.

---

## 🚀 Architectural Capabilities & Key Features

### 1. 💬 Unified AI Copilot (Qwen-2.5-3B 4-bit)
* **Grounded Location Intelligence**: Delivers real-world expansion recommendations (e.g., Siripuram, RK Beach, MVP Colony for Visakhapatnam; HITEC City, Gachibowli, Jubilee Hills for Hyderabad).
* **Multi-Agent Orchestration**: Synthesizes operational inputs across Workforce Attrition, Outlet Performance, and Supply Chain Risk agents into single unified decisions.
* **Structured Output Generation**: Generates automated JSON audit payloads alongside natural language explanations.

### 2. 👥 Agent 1: Workforce Attrition Risk Predictor
* **Telemetry Sliders**: Interactive controls for weekly overtime hours and job satisfaction scores.
* **Uncertainty Quantification**: Displays dynamic 95% Wilson Score confidence intervals for attrition probabilities.
* **AI Retention Strategies**: Synthesizes structured retention plans via LLM reasoning.

### 3. 🏬 Agent 2: Outlet Expansion & Performance Predictor
* **Tier & Clustering Logic**: Classifies new store proposals into operational clusters (Tier 1 Apex, Tier 2 Stable, etc.).
* **Financial Modeling**: Predicts monthly outlet revenue ($R^2 \ge 0.90$) based on footfall, staffing levels, and operational expenditure.

### 4. 📦 Agent 3: Supply Chain & Weather Inventory Advisor
* **Localized Weather Telemetry**: Factors in real-time weather impacts ($\pm X\%$) and logistics lead-time delays (+X days).
* **SKU Criticality Matrix**: Plotly-based stockout risk heatmaps across core inventory SKUs (Coffee Beans, Eco Cups, Syrups).
* **Automated Reorder Queue**: Ranks reorder priority based on stockout vulnerability and safety stock buffers.

### 5. 🛡️ Enterprise Security & Admin Controls
* **Dual Recovery Password Reset**: Supports real Gmail SMTP OTP dispatch (via `sanviworks123@gmail.com`) or hashed Security Question verification.
* **Rate Limiting**: Exponential OTP resend cooldowns ($60\text{s} \rightarrow 180\text{s} \rightarrow 300\text{s} \rightarrow 1\text{hr}$).
* **Progressive Lockout**: Progressive lockout protection (3 strikes = 5m, 4 strikes = 15m, 5 strikes = Permanent Admin lock).
* **Password Strength Checker**: Real-time password validation badges (`Weak` / `Average` / `Good`).
* **Admin Dashboard**: Comprehensive user lifecycle management (Add, Delete, Unlock accounts) and ML Model Card audit tables.

---

## 📊 Port & Service Coverage Table

| Port / Protocol | Service / Component | Function & Scope |
| :--- | :--- | :--- |
| **Port 8501 (HTTP)** | Streamlit Web Application | Main UI hosting AI Copilot, Agent Modules, Analytics, and Admin Portal |
| **Port 587 (TLS)** | Gmail SMTP Dispatch | Real-time OTP email delivery for account recovery |
| **Port 443 (HTTPS)** | HuggingFace & Pyngrok / Localtunnel | Model weight retrieval (Qwen-2.5-3B) and public tunnel creation |
| **SQLite (In-Memory/File)** | Relational Database | User auth, failed attempt logs, chat history, and model performance metrics |

---

## 📈 Multi-Algorithm Model Comparison Matrix

Over **5 machine learning algorithms** were evaluated per agent module to optimize metrics:

| Agent Module | Evaluated Algorithms | Primary Target Metric | Optimal Model Achieved |
| :--- | :--- | :--- | :--- |
| **Agent 1: Workforce** | RandomForest, GradientBoosting, ExtraTrees, LogisticRegression, SVC | ROC-AUC / Accuracy | **RandomForest (94.2% Accuracy, 0.965 ROC-AUC)** |
| **Agent 2: Outlets** | GradientBoosting, RandomForest, Ridge, AdaBoost, ExtraTrees | $R^2$ Score ($\ge 0.90$) / RMSE | **GradientBoosting ($R^2 = 0.941$, $\text{RMSE} = 12,450$)** |
| **Agent 3: Inventory** | RandomForest, GradientBoosting, ExtraTrees, AdaBoost, LogisticRegression | ROC-AUC / Accuracy | **RandomForest (95.6% Accuracy, 0.978 ROC-AUC)** |

---

## 📸 System Screenshots & Interface Demonstration

### 1. Secure Access Gate (Login View)
*A centered portal layout featuring role-based authentication, empty-field blocking alerts, and real-time validation.*
<img width="1334" height="650" alt="image" src="https://github.com/user-attachments/assets/80feb31b-bffe-4727-96ef-03ff501b66e2" />
After the login:
<img width="369" height="745" alt="image" src="https://github.com/user-attachments/assets/70267ab5-1520-41b3-8d00-9c4fa43517a5" />

### 2. AI Copilot (Prompt + Real Location Response)


*Unified Qwen-2.5-3B Copilot returning real-world neighborhood recommendations and multi-agent synthesis.*
<img width="1394" height="415" alt="image" src="https://github.com/user-attachments/assets/309cbfdd-9200-440c-90c5-bf5f102de643" />
<img width="1337" height="256" alt="image" src="https://github.com/user-attachments/assets/0e4df89b-a716-4fad-8b2f-e9058b4b0776" />
<img width="1358" height="544" alt="image" src="https://github.com/user-attachments/assets/797dede1-6fe7-4fe2-b657-4c70124f5894" />
<img width="1363" height="282" alt="image" src="https://github.com/user-attachments/assets/771aef07-9f46-4e1d-8ef8-65b60ce3f438" />



### 3. ML Pricing & Attrition Predictor (Input + Predictions)
*Interactive workforce sliders showing real-time attrition risk calculation, 95% confidence intervals, and LLM strategies.*

<img width="1455" height="429" alt="image" src="https://github.com/user-attachments/assets/7d9078bc-c7ce-4e61-bb1f-dea0562e9513" />
<img width="1465" height="724" alt="image" src="https://github.com/user-attachments/assets/1f4a9368-c517-4477-b55f-10dce41e2d9e" />

### 4. Admin Panel — ML Model Cards
*Audit table displaying metrics ($R^2$, RMSE, Accuracy, ROC-AUC) across 5+ evaluated algorithms per agent.*
<img width="1365" height="660" alt="image" src="https://github.com/user-attachments/assets/e8e6655b-a3a7-4ed7-a60c-eb7470b259e2" />



### 5. Admin Panel — User Lifecycle Management
*User table with controls to Add, Delete, or Unlock user accounts.*
<img width="1388" height="599" alt="image" src="https://github.com/user-attachments/assets/d199bffb-7d22-412b-8313-08ca72b70371" />


### 6. Progressive Security Lockout & OTP Cooldown Notice
*Triggered lockout message after failed login attempts alongside the OTP rate-limiting cooldown indicator.*
<img width="1190" height="753" alt="image" src="https://github.com/user-attachments/assets/1c3bcede-3a36-4356-9fef-0e289a01f7fd" />

