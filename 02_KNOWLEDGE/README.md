# Structured Knowledge

Цей каталог містить структуроване knowledge, вилучене з canonical transcripts.

Підкаталоги:
- ARCHITECTURE
- BUSINESS_LOGIC
- REQUIREMENTS
- WORKFLOWS
- DATA
- INTEGRATIONS

Кожен knowledge item повинен:
- мати стабільний ID;
- мати status;
- мати source CALL-ID;
- не суперечити наявному knowledge без explicit conflict;
- розширювати існуючий item, якщо knowledge вже існує.

`00_INDEX/TOPIC_INDEX.md` є маршрутизатором до цього knowledge. Topic entry не дублює зміст KB-файлу.

Agent не повинен створювати дублікати лише через новий transcript або нову назву тієї самої теми.