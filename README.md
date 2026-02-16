<img src="images/readme-banner-dark.svg" width="1000">

# SOC 監控與事件處理架構實驗室  
### SOC Monitoring & SIEM Architecture Lab

本專案展示一套整合式 Monitoring 與 SIEM 架構模型，
強調事件生命週期設計、事件關聯能力、
以及長期可持續維運的架構思維。

---

# 🧭 SOC = 企業資安戰情中心

<img src="images/soc-command-center-model-dark.svg" width="1000">

SOC 可以理解為企業的「資安戰情中心」，  
但真正的價值不只是即時告警，而是：

- 事件如何被關聯
- 是否能建立完整時間軸
- 是否能快速判斷 Root Cause
- 是否能長期優化監控策略

---

# 🏗 架構總覽（五層模型）

<img src="images/architecture-overview-dark.svg" width="1000">

五層能力堆疊：

1. Detection – Zabbix / Wazuh / Zeek  
2. Correlation – Graylog  
3. Root Cause Analysis  
4. Trend Validation – Prometheus  
5. Operational Sustainability – Maintenance SOP  

---

# 🔔 告警 × 關聯架構

<img src="images/alert-correlation-architecture-dark.svg" width="1000">

設計重點：

- Trigger 產生告警
- Email 通知
- 日誌集中與時間軸建立
- 根因判斷
- 趨勢驗證
- 長期優化

---

# 🔁 Incident Lifecycle Workflow

<img src="images/incident-workflow-dark.svg" width="1000">

完整流程：

Detection → Notification → Correlation → Root Cause → Trend & Optimize

---

# 🔧 Zabbix 功能展示

- Agent 存活監控
- Service restart 偵測
- Problem / Recovery 狀態追蹤
- Downtime 計算
- Email 通知

---

# 🔗 Zabbix × Graylog 關聯展示

1. Zabbix 偵測異常  
2. 發送通知  
3. Graylog 收集相關日誌  
4. 建立完整時間軸  
5. 協助判斷是否為 Crash / Manual Restart / Attack Chain  

---

# ⚠ 為什麼許多 SOC 會失敗？

- Alert fatigue
- 缺乏事件關聯能力
- 工具堆疊但沒有分層
- 沒有長期維運策略

---

# 💡 本專案解決思路

- 分層責任清楚
- 事件生命週期模型
- 關聯與時間軸優先
- 維運節奏設計

---

# 🛠 Maintenance SOP

- 每日：健康檢查
- 每週：告警降噪
- 每月：容量與 retention 檢視
- 每季：升級與還原演練

---

# 🌍 English Summary

This repository demonstrates a layered SOC monitoring architecture
focusing on event correlation, incident lifecycle modeling,
and long-term operational sustainability.

It rebuilds SOC core capabilities from first principles.
