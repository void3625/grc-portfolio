# Oscorp 敏感資料 IAM 存取控制案例

> 本案例為 GRC / Identity and Access Management 學習過程中的模擬案例，非實際客戶專案。  
> 主要目的為練習敏感資訊的存取控制、最小權限、特權帳號管理與存取權限審查。

## 1. 案例背景

Oscorp 成功推出一款新藥，而藥物的秘密配方屬於公司最敏感的資訊資產之一。

與配方相關的文件與資料皆儲存在 Microsoft SQL Server 2022 資料庫中。

在模擬 Assessment（評估）中發現：

- 所有 Research Lab 成員皆具有配方資料的 Read Access（讀取權限）。
- Harry Osborne 擁有資料庫完整的 Administrator Access（管理員權限）。
- 使用者目前僅透過 Username 與 Password 登入系統。

由於該配方屬於高度敏感的 Intellectual Property（智慧財產），現有的 Identity and Access Management, IAM（身分與存取管理）控制存在改善空間。

---

## 2. 問題與風險

### 2.1 過度授權

目前所有 Research Lab 成員皆能讀取完整配方。

員工屬於研究部門，並不代表其工作一定需要接觸完整配方。

過多的使用者具有存取權限，會增加：

- 帳號遭竊後造成資料外洩的可能性
- 員工誤傳敏感資訊的風險
- Insider Threat（內部威脅）
- 人員異動後未即時撤銷權限的風險

因此目前的權限設計不符合 Principle of Least Privilege（最小權限原則）。

### 2.2 特權帳號權限過大

Harry Osborne 長期具有完整 Database Administrator 權限。

如果日常工作並不需要完整管理權限，持續保留 Full Admin Access 會增加：

- 誤操作
- 未授權修改
- 帳號遭入侵後的影響範圍
- Privileged Account Abuse（特權帳號濫用）

### 2.3 Authentication（身分驗證）強度不足

系統僅使用帳號與密碼登入。

如果密碼因 Phishing（網路釣魚）、Credential Theft（憑證竊取）或 Password Reuse（密碼重複使用）而外洩，攻擊者可能直接取得系統存取權限。

---

## 3. 我的分析

我認為此案例的核心不是單純「把權限全部收緊」，而是根據：

- Job Responsibility（工作職責）
- Business Need（業務需求）
- Data Sensitivity（資料敏感度）

決定每個使用者真正需要的存取權限。

因此，Research Lab 成員不應因為隸屬同一部門，就自動取得秘密配方的存取權。

存取權限應建立在明確的 Business Justification（業務正當性）之上。

同時，對於高權限帳號，應將日常帳號與 Administrator Account（管理員帳號）區分，避免長期使用高權限帳號執行一般工作。

---

## 4. 控制措施／處理方式

### 4.1 Principle of Least Privilege

重新檢視所有可以存取配方的使用者。

只有工作上真正需要存取完整配方的人員才能保留權限。

### 4.2 Role-Based Access Control, RBAC（角色型存取控制）

依照不同工作職責設計角色，例如：

- General Researcher
- Formula Researcher
- Database Administrator

不同角色只取得其工作所需的資料與操作權限。

### 4.3 Multi-Factor Authentication, MFA（多因素驗證）

針對敏感資料庫與高權限帳號導入 MFA，以降低帳號密碼外洩後直接被利用的風險。

### 4.4 Privileged Access Management, PAM（特權存取管理）

Harry 不應以 Full Admin 帳號進行日常工作。

建議：

- 使用 Standard Account（日常一般帳號）進行一般作業
- 只有需要執行管理工作時才提升權限
- 高權限操作應經過授權
- 如系統與環境允許，可使用 Just-In-Time, JIT（即時權限）限制特權存取時間

### 4.5 User Access Review（使用者存取權限審查）

定期確認：

- 使用者是否仍在原本的職務
- 是否仍有 Business Need
- 是否存在過度授權
- 離職或調職人員權限是否已撤銷

---

## 5. Audit / GRC 思考

如果我是 Auditor（稽核人員），我不只會確認公司是否有 Access Control Policy。

我還會確認控制是否真正運作。

例如我會要求：

- Current User Access List（目前使用者權限清單）
- User Role / Job Function（使用者職務）
- Access Request Record（權限申請紀錄）
- Manager Approval（主管核准紀錄）
- Privileged Account List（特權帳號清單）
- Periodic Access Review Evidence（定期權限審查證據）

並將「實際具有權限的人」與「工作上真正需要權限的人」進行比較。

如果發現使用者沒有合理 Business Justification 卻仍可存取敏感配方，就可能構成 Access Control Exception（存取控制例外）。

---

## 6. 我從這個案例學到什麼

這個案例讓我理解：

IAM 並不是單純要求更多驗證機制，而是需要回答：

> Who should have access to what, why, and for how long?

也就是：

- 誰可以存取
- 可以存取什麼
- 為什麼需要存取
- 可以存取多久
- 如何證明該權限曾經被正確核准與定期檢查

我也了解到，即使只是 Read Access（讀取權限），如果敏感資料的存取人數過多，仍然會增加資料外洩的風險。

因此，Least Privilege、RBAC、Privileged Access Management 與 Access Review 應該相互配合，而不是單獨存在。
