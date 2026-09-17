# n8n 每日 AI 情報官（n8n Daily AI Intel Agent）

以 **n8n（self-hosted）** 打造的 AI Agent 每日情報推播系統：

**排程抓取 AI 領域新資訊（arXiv + Hacker News）→ LLM 判讀重要性與中文摘要 → AI Agent 自主決定深入哪些項目 → Telegram 推播每日彙總簡報。**

> 作品集專案 — 展示 **Agentic AI workflow** 的設計、實作與交付；所有 workflow 以 JSON 版控（可匯入重現）。

## 專案狀態（里程碑）

- [x] **M1** 環境建置與 n8n 核心概念
- [x] **M2** arXiv 抓取與解析
- [x] **M3** 排程 + Telegram 通知
- [x] **M4** LLM 判讀（摘要 + 評分）
- [x] **M5** AI Agent 節點（自主策展）★ 核心
- [x] **M6** 去重（狀態管理）
- [ ] **M7** 錯誤處理與可觀測性
- [ ] **M8** 交付包裝

## 快速開始

```bash
# 1. 複製環境變數範本（Windows PowerShell）
copy .env.example .env

# 2. 啟動 n8n
docker compose up -d

# 3. 開啟 UI
#    http://localhost:5678
```

首次開啟需建立 n8n 管理者帳號（只存在本機，不上傳）。

## 目錄結構

```
n8n-daily-ai-intel-agent/
├── docker-compose.yml      # n8n 服務定義（時區 / 持久化 volume）
├── .env.example            # 環境變數範本（複製成 .env 使用）
├── .gitignore
├── workflows/              # 匯出的 workflow JSON（版控）
└── README.md
```

## 架構

（M2 起逐步補上資料流圖）
