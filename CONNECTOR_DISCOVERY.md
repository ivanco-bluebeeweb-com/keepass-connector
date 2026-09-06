# KeePass Connector — Connector Discovery

**Official Documentation:** https://keepass.info  
**Base URL:** Local RPC / KeePassHTTP / File Parser (No cloud API)  
**Auth Model:** Master Password / Keyfile / KeePassHTTP RPC Key  

## Основные сущности вендора
- записи паролей (entries), группы (groups), ключевые файлы (keyfiles), хеши целостности

## Лимиты и особенности API
- Соблюдение Rate Limits вендора, обработка HTTP 429 с экспоненциальным backoff.
- Валидация входных данных по Pydantic-схемам вендора до отправки запроса.
- Тестовая точка проверки подключения: `Local database unlock verification`.
