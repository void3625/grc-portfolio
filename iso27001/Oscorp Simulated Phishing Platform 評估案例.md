# Oscorp Simulated Phishing Platform 評估案例

> 本案例為 GRC / ISO 27001 學習過程中的模擬案例，非實際客戶專案。  
> 主要目的為練習 Security Awareness（資安意識）、Risk Treatment（風險處理）、Control Effectiveness（控制有效性）與 Audit Evidence（稽核證據）的分析方式。

---

## 1. 案例背景

Oscorp 目前只有一套在員工入職時完成的 Security Awareness Training（資安意識訓練）。

該訓練自 2013 年公司成立時導入，內容主要為一般性的資訊安全提醒。公司目前沒有建立持續性的訓練、模擬釣魚測試或成效衡量機制。

近期，一家資安廠商向 CEO 推薦 Simulated Phishing Platform（模擬釣魚平台），希望透過定期模擬釣魚郵件，降低員工遭受 Phishing（網路釣魚）與 Social Engineering（社交工程）攻擊的風險。

CEO 因公司近期有額外預算，因此希望評估是否值得投資此平台。

---

## 2. 問題與風險

我不會因為公司有多餘預算，或因為廠商認為「Human Element is the weakest link」，就直接建議購買平台。

我會先進行 Gap Analysis（落差分析），確認 Oscorp 目前的 Security Awareness Controls（資安意識控制）與期望狀態之間的差異。

目前可能存在的問題包括：

| 問題 | 可能造成的風險 |
|---|---|
| Security Awareness Training 僅在入職時進行一次 | 員工可能逐漸忘記訓練內容 |
| 教材長期未更新 | 無法反映新的 phishing 與 social engineering 手法 |
| 沒有持續測試 | 無法確認員工實際辨識 phishing 的能力 |
| 沒有量化指標 | 管理階層無法判斷控制是否有效 |
| 缺乏明確通報機制 | 員工遇到可疑郵件時可能不知道如何處理 |

因此，Oscorp 的主要問題不只是「員工可能被 phishing」，而是：

> 組織目前缺乏足夠的 Evidence（證據）與 Metrics（指標），證明 Security Awareness Controls 是否持續有效。

---

## 3. 我的分析

我會依照以下邏輯評估是否需要導入模擬釣魚平台：

### 3.1 Risk

先確認 Oscorp 真正面對的 phishing risk。

例如攻擊者可能透過 phishing：

- 竊取員工帳號密碼
- 傳播 malware
- 取得內部系統初始存取權
- 竊取 pharmaceutical research data
- 進一步進行 lateral movement

由於 Oscorp 擁有敏感的藥物研發資料，因此 phishing 可能成為攻擊者取得內部存取權限的重要入口之一。

### 3.2 Existing Controls

目前主要控制只有：

- Onboarding Security Awareness Training

但該控制缺乏：

- 定期更新
- 實際測試
- 成效監控
- 可量化 metrics

因此無法確認控制是否仍然有效。

### 3.3 Control Gap

目前最大的 Control Gap（控制缺口）在於：

> Oscorp 無法確認員工是否真的能在實際情境中辨識、避免並回報 phishing email。

### 3.4 Treatment Option

如果 phishing 被評估為重要風險，而且現有 Security Awareness Controls 不足，我才會考慮將 Simulated Phishing Platform 作為 Risk Treatment（風險處理）的一部分。

因此我的分析邏輯是：

**Risk → Existing Control → Control Gap → Treatment Option**

而不是：

**Vendor Recommendation → Purchase Tool**

---

## 4. Simulated Phishing Platform 如何運作

Simulated Phishing Platform 並不只是單純「寄一封假的 phishing email」。

它通常是一個完整的 Security Awareness Testing 流程。

基本流程可以整理為：

**Define Objective  
→ Select Target Group  
→ Design Scenario  
→ Send Simulation  
→ Track Employee Behavior  
→ Provide Training  
→ Analyze Metrics  
→ Improve Program**

### 4.1 定義測試目標

首先需要確認這次 campaign 想測試什麼。

例如：

- 員工是否會點擊 suspicious link
- 員工是否會輸入 credential
- 員工是否會開啟 attachment
- 員工是否會主動 Report Phishing

### 4.2 設計情境

實務上通常不需要每次從零開始手工寫 phishing email。

許多平台會提供：

- Email Templates
- Landing Pages
- Reporting Mechanism
- Tracking Dashboard
- Training Modules

內部 Security Team 可以根據公司的業務情境進行調整。

例如 Oscorp 可以使用較貼近實際工作的模擬情境：

- Pharmaceutical research update
- HR policy change
- Internal document sharing
- Password reset notification
- Benefits or payroll update

重點不是把 phishing email 做得多「厲害」，而是測試情境是否與組織實際風險相關。

### 4.3 執行模擬測試

平台寄送模擬 phishing email 後，可以記錄員工的行為。

例如：

- 是否開信
- 是否點擊連結
- 是否輸入 credential
- 是否回報 phishing
- 是否完成後續 training

這些資料可以成為後續 Security Awareness Program 的 Metrics。

---

## 5. Metrics 與 Control Effectiveness

導入平台之後，不應只觀察 Click Rate。

應搭配多個 Metrics 來評估 Control Effectiveness（控制有效性）。

| Metric | 用途 |
|---|---|
| Click Rate | 衡量員工是否點擊可疑連結 |
| Credential Submission Rate | 衡量是否進一步提交敏感資訊 |
| Reporting Rate | 衡量員工主動回報可疑郵件的能力 |
| Repeat Failure Rate | 找出持續需要額外協助的人員 |
| Training Completion Rate | 確認相關訓練是否完成 |

例如：

第一季：

- Click Rate：20%
- Reporting Rate：5%

六個月後：

- Click Rate：8%
- Reporting Rate：45%

這樣的趨勢可以較合理地支持：

> Security Awareness Controls 正在改善員工的實際資安行為。

---

## 6. 員工多次未通過模擬測試的處理方式

如果員工多次點擊模擬 phishing email，我不認為第一步應該是處罰。

較合理的方式是依照事先建立的 Security Awareness Program 執行改善措施。

例如：

- 提供 targeted training
- 安排簡短 supplementary training
- 使用更具體的 phishing examples
- 針對高風險族群提供額外 awareness session
- 後續安排再次測試

例如某位員工連續三次未通過測試，我會先確認：

- 是否都是同一類型的情境
- 員工是否理解 phishing indicators
- 是否知道正確的 reporting process

再根據問題提供適合的教育。

目標應該是：

> 改善 Security Behavior，而不是讓員工害怕失敗或不敢通報。

---

## 7. Control Measures

若 Oscorp 決定導入平台，我認為完整的 Security Awareness Program 應包含：

### Regular Security Awareness Training

定期更新訓練內容，使其反映新的 phishing 與 social engineering threats。

### Simulated Phishing Campaign

透過實際情境測試員工行為，而不是只依賴課堂知識。

### Report Phishing Mechanism

提供清楚且容易使用的 phishing reporting channel。

### Targeted Training

對於重複失敗或高風險族群提供額外訓練。

### Continuous Monitoring

持續觀察 Metrics 與趨勢，並調整 training program。

---

## 8. Audit / GRC 思考

如果我是 Auditor，我不會只詢問：

> 你們有沒有做 Security Awareness Training？

我會要求相關 Audit Evidence，例如：

- Security Awareness Training Material
- Training Version History
- Training Completion Records
- Employee Training Logs
- Quiz / Assessment Results
- Phishing Simulation Reports
- Click Rate / Reporting Rate Metrics
- Security Awareness Policy
- Policy Approval Records
- Employee Communication Evidence
- Follow-up Training Records

我要確認的不只是控制存在，而是：

> 控制是否有被適當設計、執行、監控，並且能透過 Evidence 證明其持續有效。

---

## 9. 投資建議

我不會單純因為 Oscorp 有 excess budget 就建議購買。

我的建議是：

> 先確認 phishing risk、現有 Security Awareness Controls 與 Control Gap。  
> 如果組織目前缺乏持續訓練、實際測試與量化指標，Simulated Phishing Platform 可以作為改善 Security Awareness Program 的其中一項控制措施。

但平台不應被視為完整解決方案。

比較合理的 Security Awareness Lifecycle 是：

**Training  
→ Simulation  
→ Reporting  
→ Metrics  
→ Review  
→ Improvement**

---

## 10. 我從這個案例學到什麼

這個案例讓我理解，GRC 的角色並不是看到一個 Security Tool 就判斷「好不好用」。

更重要的是先確認：

1. 我們正在處理什麼 Risk？
2. 現有 Controls 是什麼？
3. Controls 是否真的有效？
4. 存在哪些 Control Gaps？
5. 新工具能不能合理補足這些缺口？
6. 導入之後要如何透過 Metrics 與 Evidence 證明有效？

我也學到，Simulated Phishing 的目的不應只是找出「誰做錯了」，而是透過測試、教育與持續改善，提升整個組織對 phishing 的辨識與回報能力。
