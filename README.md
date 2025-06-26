# 🐋 Whale Sentinel Agents

[![Horusec Security Scan](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/horusec-scan.yml/badge.svg?branch=dev)](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/horusec-scan.yml)
[![Build on Release](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/build-on-release.yml/badge.svg?branch=main)](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/build-on-release.yml)

---

## 🧠 About Whale Sentinel Agents

Whale Sentinel Agents are lightweight runtime security modules that monitor, analyze, and optionally block HTTP requests in Python web applications. They provide intelligent protection and visibility by collecting and analyzing metadata at runtime.

These agents are plug-and-play components designed for frameworks like Flask, FastAPI, and Django. Once integrated and configured, they silently monitor or actively defend your application based on the selected operation mode.

---

## 📦 Releases

| No. | Language | Framework        | Support            | Agent                          | Agent Version |
|-----|----------|------------------|---------------------|--------------------------------|----------------|
| 1   | Python   | Flask >= 3.0.0   | ✅                  | `whale-sentinel-flask-agent`   | 0.1.1          |
| 2   | Python   | FastAPI >= 0.15.0| ✅                  | `whale-sentinel-fastapi-agent` | 0.1.1          |
| 3   | Python   | Django >= 5.2.0  | ✅                  | `whale-sentinel-django-agent`  | 0.1.1          |

---

## 🚀 Operation Modes

The agent supports four operation modes defined in its runtime profile:

| Mode         | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `off`        | Disables protection. Requests are passed through without interception.     |
| `lite`       | Collects lightweight request metadata and sends it asynchronously.         |
| `monitor`    | Full request inspection with no blocking. Useful for passive analysis.     |
| `protection` | Full active defense. Malicious requests may be blocked in real-time.       |

### 🔐 Additional Feature

- `secure_response_headers`: If enabled, security headers (e.g., `X-Frame-Options`, `X-Content-Type-Options`) will be added to outgoing responses.

---

## 🧾 Metadata Collected by Agent

Each request may trigger a metadata payload sent to Whale Sentinel backend or stored locally. This includes:

### 1. Agent Information
- `agent_id`
- `agent_name`

### 2. Client Information
- `ip`
- `device_type`
- `platform`
- `browser`, `browser_version`
- `network_type`

### 3. HTTP Request Information
- `method`, `url`, `scheme`, `host`, `endpoint`
- `headers`: user-agent, content-type, content-length, referrer
- `body`, `query_parameters`

### 4. Uploaded Files Metadata (if any)

- `file_name`: Name of the uploaded file
- `file_size`: File size in bytes
- `file_type`: MIME type of the file
- `file_content`: Base64-encoded content of the file
- `file_hash256`: SHA-256 hash of the file content

### 5. Runtime Environment

- `ip_address`, `pid`, `run_as`
- `executable_path`, `executable_name`, `executable_version`
- `process_name`, `process_path`, `process_command`
- `platform`, `cpu_usage`, `memory_usage`
- `architecture`, `os_name`, `os_version`, `os_build`

### 6. Timestamps
- request_created_at: UTC timestamp in ISO 8601 format

### 📄 License

This project is licensed under the MIT License.

### 🛡️ Security & Reporting

If you discover a vulnerability, please report it responsibly via GitHub Issues or contact the maintainers privately.