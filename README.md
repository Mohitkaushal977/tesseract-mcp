# 🚀 Tesseract AI Platform Manager — Remote MCP Server

[![Smithery Marketplace](https://smithery.ai/badge/tesseract)](https://smithery.ai/server/tesseract)

Official Model Context Protocol (MCP) server for **Tesseract AI**.

- **SSE Endpoint**: `https://prod2.adlift.com/mcp/sse`
- **ChatGPT OpenAPI Spec**: `https://prod2.adlift.com/static/openapi_tesseract_mcp.json`
- **Homepage**: [tesseract.adlift.com](https://tesseract.adlift.com)

---

## 🌟 Capabilities & Tools

1. **`request_login_otp(email)`**: Sends a 6-digit OTP code to the user's email for passwordless authentication.
2. **`verify_login_otp(email, otp_code)`**: Authenticates the session with the 6-digit OTP code.
3. **`login_user(email, password)`**: Authenticates using standard user credentials.
4. **`get_user_details(email)`**: Retrieves account details, role, department, subscription status, and shared projects.
5. **`list_all_users(query, limit)`**: Search Tesseract user accounts.
6. **`list_projects(query)`**: List active SEO projects and target domains.
7. **`share_project_with_user(project_id, email)`**: Grants project access to another user.
8. **`unshare_project_from_user(project_id, email)`**: Removes project access from a user.
9. **`signup_user(email, subscription_type)`**: Registers a new user (defaults to 7-day Free Plan).
10. **`update_user_subscription(email, subscription_type)`**: Updates a user's subscription plan (Basic, Pro, Enterprise).
11. **`adhoc_llm_search(brand_name, brand_url, keywords, competitors, country)`**: Runs real-time ad-hoc LLM visibility analysis across ChatGPT, Gemini, Perplexity, DeepSeek, Claude, and Google AI Mode.

---

## 🔌 How to Connect

### 1. Claude Web (`claude.ai`) & Claude Desktop
Add a new Custom SSE Connector in Settings ➔ Connectors:
- **Server Name**: `Tesseract`
- **SSE Endpoint**: `https://prod2.adlift.com/mcp/sse`

### 2. ChatGPT Custom Actions
Import this OpenAPI spec URL into your GPT Editor:
- **URL**: `https://prod2.adlift.com/static/openapi_tesseract_mcp.json`

### 3. Smithery.ai 1-Click Install
Install directly from Smithery:
```sh
npx -y @smithery/cli run tesseract --config "{}"
```

---

## 🔒 Security & Privacy
All Tesseract tools require an active authenticated session (`request_login_otp` + `verify_login_otp` or `login_user`) before executing actions.
