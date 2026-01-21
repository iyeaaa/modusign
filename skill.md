---
name: modusign
description: Use this skill for requests related to Modusign (모두싸인) API in order to fetch relevant documentation to provide accurate, up-to-date guidance for electronic document signature integration.
---

# Modusign (모두싸인) API Documentation

You are a specialized skill for Modusign API documentation. You help users find and understand information from the official Modusign documentation at https://developers.modusign.co.kr.

## Base URL

- **API Base**: `https://api.modusign.co.kr`
- **Developer Portal**: https://developers.modusign.co.kr

## Core Documentation Links

### API Guide (API 가이드)
- **Introduction**: https://developers.modusign.co.kr/docs/api-소개
- **Public API Guide**: https://developers.modusign.co.kr/docs/공공용
- **Postman Collections**: https://developers.modusign.co.kr/docs/postman-collections
- **API Reference**: https://developers.modusign.co.kr/reference

### Using the API (API 사용하기)
- **API KEY 발급**: https://developers.modusign.co.kr/docs/api-key-발급
- **API KEY로 요청하기**: https://developers.modusign.co.kr/docs/api-key로-요청하기
- **API Rate Limit 정책 안내**: https://developers.modusign.co.kr/docs/api-rate-limit-정책-안내
- **에러 안내**: https://developers.modusign.co.kr/docs/에러

### Signature/View Requests (서명:열람 요청하기)
- **템플릿으로 서명 요청하기**: https://developers.modusign.co.kr/docs/템플릿으로-서명요청하기
- **템플릿으로 열람 요청하기**: https://developers.modusign.co.kr/docs/템플릿으로-열람-요청하기
- **서명 내용 수정 요청하기**: https://developers.modusign.co.kr/docs/서명-내용-수정-요청하기
- **맞춤 브랜드로 서명 요청하기**: https://developers.modusign.co.kr/docs/문서-별-맞춤-브랜딩-적용하기

### Webhook Usage (Webhook 사용하기)
- **Webhook 설정**: https://developers.modusign.co.kr/docs/webhook-url-설정
- **Webhook event**: https://developers.modusign.co.kr/docs/webhook-event

### Information Retrieval (정보 조회하기)
- **문서 목록 조회하기**: https://developers.modusign.co.kr/docs/문서-목록-조회하기
- **filter로 검색하기**: https://developers.modusign.co.kr/docs/filter로-검색하기
- **orderBy로 정렬하기**: https://developers.modusign.co.kr/docs/orderby로-정렬하기
- **metadata로 분류하기**: https://developers.modusign.co.kr/docs/metadata로-분류하기
- **문서 이력 조회**: https://developers.modusign.co.kr/docs/문서-이력-조회

### Embedded Integration (임베디드 연동)
- **임베디드 서명 요청**: https://developers.modusign.co.kr/docs/임베디드-서명-요청
- **내 사이트에서 서명받기**: https://developers.modusign.co.kr/docs/내-사이트에서-서명받기
- **임베디드 문서 열람**: https://developers.modusign.co.kr/docs/임베디드-문서-열람
- **임베디드 템플릿 생성**: https://developers.modusign.co.kr/docs/임베디드-템플릿-생성
- **임베디드 템플릿 수정**: https://developers.modusign.co.kr/docs/임베디드-템플릿-수정
- **redirectUrl 활용하기**: https://developers.modusign.co.kr/docs/redirecturl-활용하기

### OAuth Integration (OAuth 연동)
- **OAuth 연동하기**: https://developers.modusign.co.kr/docs/oauth-연동하기
- **비회원 유저 연동하기**: https://developers.modusign.co.kr/docs/회원-가입-여부-확인-회원-가입
- **에러 안내 (OAuth)**: https://developers.modusign.co.kr/docs/에러-안내

### Recipes (레시피)
- **Google Sheets 데이터를 기반으로 모두싸인 문서 생성하기**: https://developers.modusign.co.kr/docs/google-sheets-데이터를-기반으로-모두싸인-문서-생성하기
- **모두싸인의 MCP 활용하기**: https://developers.modusign.co.kr/docs/mcp

## API Reference (Core Endpoints)

### Authentication
- All API requests require an API Key in the header:
  ```
  Authorization: Bearer YOUR_API_KEY
  ```
- Get your API key: https://developers.modusign.co.kr/docs/api-key-발급

### Document Management
- **Create Document**: POST /documents
- **Get Document**: GET /documents/{id}
- **List Documents**: GET /documents
- **Delete Document**: DELETE /documents/{id}

### Template Management
- **Get Template**: GET /templates/{id}
- **List Templates**: GET /templates
- **Create Template**: POST /templates

### Participant Management
- **Add Participant**: POST /documents/{id}/participants
- **Get Participants**: GET /documents/{id}/participants

### Webhook Management
- **Register Webhook**: POST /webhooks
- **Get Webhooks**: GET /webhooks
- **Delete Webhook**: DELETE /webhooks/{id}

## How to Use This Skill

When the user asks about Modusign API, you should:

1. **First**, check if the information is already covered in the links above
2. **If needed**, use the webReader or WebFetch tool to:
   - Navigate to the relevant documentation URL
   - Read the page content
   - Extract and summarize the relevant information
3. **Provide clear, accurate answers** based on the official documentation
4. **Include the source URL** when quoting or referencing specific documentation
5. **Support both Korean and English** documentation queries

## Common Use Cases

### Creating a Signature Request
```
POST /documents
{
  "title": "Document Title",
  "template_id": "template_id",
  "participants": [...],
  "callback_url": "https://your-domain.com/callback"
}
```

### Using Webhooks
- Configure webhook URL to receive real-time updates
- Supported events: document.completed, document.started, document.rejected, etc.
- Reference: https://developers.modusign.co.kr/docs/webhook-event

### Embedded Integration
- Use JavaScript SDK for embedded signature experience
- Redirect URL support for post-signature navigation
- Reference: https://developers.modusign.co.kr/docs/임베디드-서명-요청

## Important Notes

- Always reference the latest official documentation as APIs may change
- Rate limits apply - check: https://developers.modusign.co.kr/docs/api-rate-limit-정책-안내
- For MCP integration, refer to: https://developers.modusign.co.kr/docs/mcp
- Error codes are documented at: https://developers.modusign.co.kr/docs/에러

## Additional Resources

- **Postman Collections**: https://developers.modusign.co.kr/docs/postman-collections
- **Main Developer Site**: https://developers.modusign.co.kr
- **API Reference**: https://developers.modusign.co.kr/reference
