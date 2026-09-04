# Oscorp 資安稽核計畫
## Three Lines Model（三道防線模型）案例分析

> 本案例為 GRC / ISO 27001 學習過程中的模擬情境，並非實際客戶專案。  
> 主要目的為練習資安治理、控制監督與稽核角色的區分。

---

## 一、案例背景

Oscorp 近期完成高度機密的新藥研發，因此需要保護相關研究資料、智慧財產與資訊系統。

CEO 希望建立一套 Cybersecurity Audit Program（資安稽核計畫），確保公司的資訊安全控制不只是被建立，也能定期確認是否持續且有效運作。

本案例使用 Three Lines Model（三道防線模型）設計資安治理與查核架構。

---

## 二、第一線：Cybersecurity Operations

第一線是實際執行與維護資安控制的人員。

例如：

- Firewall Management
- Incident Response
- Access Control
- Vulnerability Management

第一線除了日常執行控制，也應定期進行 Control Self-Assessment（控制自我評估）。

例如 Firewall Team 可以每季檢查：

- 是否存在已過期的 Firewall Rules
- 是否有過度寬鬆的 Any-to-Any Rules
- 每一條 Rule 是否有明確的 Owner
- Rule 是否仍具有有效的 Business Requirement

這些檢查仍屬於第一線，因為是由控制執行者自行檢視其負責的控制。

---

## 三、第二線：Cybersecurity GRC / Risk & Compliance

第二線主要負責 Monitoring（監督）、Control Testing（控制測試）以及 Challenge（質疑與挑戰）。

Cybersecurity GRC 或 Risk & Compliance 人員可以確認第一線是否依照 Policy（政策）與 Standard（標準）執行控制。

例如針對 Firewall Rule Review，第二線可以要求第一線提供：

- Firewall Rule Review 紀錄
- Review 日期
- 執行人員
- 發現的 Exception（例外事項）
- Remediation（改善）追蹤紀錄
- 必要的系統報表或截圖

第二線的目的不是取代第一線操作設備，而是確認控制是否確實執行，並對異常或風險提出 Challenge。

---

## 四、第三線：Internal Audit

第三線由 Internal Audit（內部稽核）提供 Independent Assurance（獨立確信）。

Internal Audit 應獨立驗證資安控制的設計與實際執行情況，而不能只依賴第一線或第二線的說法。

例如 Internal Audit 可以抽樣 Firewall Rules，確認：

1. Rule 是否有正式申請與批准紀錄
2. Rule 是否仍具有業務需求
3. 高風險 Rule 是否經過適當審核
4. 定期 Firewall Review 是否確實執行
5. 發現的問題是否完成改善

稽核過程可以透過：

- 文件檢視
- 訪談
- 抽樣
- 系統產生的 Audit Evidence（稽核證據）

來驗證控制的有效性。

---

## 五、三道防線的核心差異

Three Lines Model 並不是讓三組人重複做相同的事情，而是建立不同程度的責任與獨立性。

- **Line 1：Do the control**
  - 執行控制
  - 維護控制
  - 進行日常自我檢查

- **Line 2：Monitor and challenge the control**
  - 監督第一線
  - 檢查控制證據
  - 追蹤風險與改善事項

- **Line 3：Independently assure the control**
  - 獨立抽樣
  - 驗證控制
  - 提供 Independent Assurance

---

## 六、我從這個案例學到的內容

透過本案例，我更清楚理解以下概念之間的差異：

- Control Execution（控制執行）
- Control Self-Assessment（控制自我評估）
- Monitoring（監督）
- Control Testing（控制測試）
- Internal Audit（內部稽核）
- Independent Assurance（獨立確信）

我也理解到 Audit Evidence（稽核證據）的重點不只是提供截圖，而是證據應具備可追溯、可驗證以及能支持控制執行情況的特性。
