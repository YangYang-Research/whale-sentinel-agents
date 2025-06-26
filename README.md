# Whale Sentinel Agents

[![Horusec Security Scan](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/horusec-scan.yml/badge.svg?branch=main)](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/horusec-scan.yml)
[![Build on Release](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/build-on-release.yml/badge.svg?branch=main)](https://github.com/YangYang-Research/whale-sentinel-agents/actions/workflows/build-on-release.yml)

| No. | Language | Framework  | Support | Agent | Agent Version | 
| --- | -------- | --------- | ------- | ----- | ------------- |
| 1 | Python | Flask >= 3.0.0 | :white_check_mark: |  whale-sentinel-flask-agent | 0.1.1 |
| 2 | Python | FastAPI >= 0.15.0 | :white_check_mark: |  whale-sentinel-fastapi-agent | 0.1.1 |
| 3 | Python | Django >= 5.2.0 | :white_check_mark: | whale-sentinel-django-agent | 0.1.1 |

# Agent Environment

Add this agent environment to your application enviroment

`WS_AGENT_ID="your_agent_id"`

`LOG_MAX_SIZE=1000000`

`LOG_MAX_BACKUP=3`

`WS_GATEWAY_API="your_whale_sentinel_gateway_api"`

`WS_AGENT_AUTH_TOKEN="your_agent_authentication_token"`

`WS_VERIFY_TLS="true"`