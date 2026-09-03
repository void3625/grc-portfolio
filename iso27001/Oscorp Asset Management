# Oscorp Asset Management 改善案例
## CMDB 與資產管理流程設計

> 本案例為 GRC / ISO 27001 學習過程中的模擬情境，並非實際客戶專案。  
> 主要目的為練習 Asset Management（資產管理）、CMDB 維護、Asset Ownership（資產責任歸屬）以及 Audit Evidence（稽核證據）思維。

---

## 一、案例背景

Oscorp 在第一次 Cybersecurity Internal Audit（資安內部稽核）中，被發現 Asset Management（資產管理）流程存在明顯缺口。

公司目前主要使用一份 spreadsheet 紀錄部分 IT systems，但內容是零散建立的，沒有完整涵蓋所有資產，也缺乏正式且持續的更新流程。

對 Oscorp 而言，這個問題不只是「資產清冊不完整」。

如果公司不知道自己有哪些系統、設備、Cloud Resources、Software 或重要資料，就無法確認這些資產是否都有被納入適當的資安控制，例如：

- Vulnerability Management
- Patch Management
- Endpoint Protection
- Backup
- Access Control
- Security Monitoring

此外，Oscorp 屬於研究導向組織，因此 Research Data（研究資料）與 Intellectual Property（智慧財產）也可能是公司最重要的資產，不能只盤點硬體設備。

因此，本案例的重點是設計一套可以持續識別、確認及維護資產資訊的流程。

---

## 二、建立完整的 Asset Inventory

首先，可以保留目前的 spreadsheet 作為 Asset Inventory（資產清冊）的起點，再逐步補充必要資訊。

例如：

- Asset ID
- Asset Name
- Asset Type
- Asset Owner
- Location
- Criticality
- Data Classification
- Status
- Last Review Date

資產範圍不應只包含 Server、Laptop 等 Hardware，也應考慮：

- Software
- Cloud / SaaS
- Database
- Business Data
- Research Data
- Intellectual Property

---

## 三、Asset Discovery 與資料確認

Oscorp 可以透過 Asset Discovery（資產探索）確認實際環境中的資產。

例如使用：

- Network Scanner
- Vulnerability Scanner
- EDR Inventory
- Active Directory
- Cloud Inventory

再將結果與現有 Asset Inventory 比對，找出：

- Missing Assets
- Duplicate Records
- Stale Records
- Shadow IT
- 已淘汰但仍存在清單中的資產

但 Automated Discovery（自動化資產探索）無法完整識別所有資訊資產。

例如研究配方或機密研究資料，因此仍需要與 IT Team、Research Team 以及 Business Stakeholders 訪談確認。

---

## 四、Asset Ownership 與 Classification

每項重要資產應指定明確的 Asset Owner（資產責任人）。

Asset Owner 不一定是實際操作系統的人，而是對資產的管理與風險負有責任的人。

同時，可以依據：

- Sensitivity（敏感度）
- Criticality（關鍵程度）

對資產進行分類。

例如 Oscorp 的 Research Intellectual Property 可能屬於高度敏感且關鍵的資產，因此應套用更嚴格的存取控制與保護措施。

---

## 五、維持 CMDB 持續更新

Asset Inventory 或 CMDB 不應只靠半年或一年一次的人工盤點維護。

較好的方式是與 Change Management（變更管理）流程整合。

例如：

- 新增 Server → 建立 CMDB Record
- 系統修改 → 更新 Asset Information
- 系統下線 → 將 Asset Status 更新為 Retired

此外，也可以定期將 CMDB 與 Scanner、EDR 或 Cloud Inventory 進行 Reconciliation（比對），確認資料與實際環境一致。

---

## 六、Audit / GRC 思考

如果我是 Auditor，我不會只確認公司是否「有一份 Asset Inventory」。

我會要求相關 Audit Evidence，例如：

- Asset Inventory / CMDB
- Asset Management Policy
- Asset Owner List
- Periodic Review Records
- Vulnerability Scanner / EDR Asset List
- Change Tickets

例如：

如果 CMDB 紀錄 120 台 Server，但 Vulnerability Scanner 發現 127 台，我會先確認額外 7 台是否真的存在，再調查為什麼沒有被納入 CMDB。

如果流程本身已經有完整設計，但人員沒有依流程更新資料，可能屬於 Operating Effectiveness（運作有效性）問題。

如果公司根本沒有定義哪些資產需要納管，或沒有建立更新機制，則可能屬於 Design Effectiveness（設計有效性）問題。

---

## 七、我從這個案例學到的內容

透過本案例，我理解到 Asset Management 並不只是維護一份設備清單。

真正重要的是建立一套持續運作的流程，確保：

- 資產能被識別
- 資產有明確 Owner
- 資產依風險進行分類
- 資產異動能及時更新
- 清冊內容能定期與實際環境進行驗證

我也理解到：

> You cannot protect what you do not know you have.

如果組織無法掌握自己的資產，就很難確保所有資產都有被納入適當的資安控制。
