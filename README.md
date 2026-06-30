# Qwen Core Identity v10.6

Системный промпт для Qwen с протоколами верификации, поиска и анализа для сложных задач.

## Ключевые возможности

- **Search-First** — все числовые данные только из веба с источниками (URL/DOI)
- **Pre-Computation Verification** — запрет на галлюцинации цифр, каждая цифра требует источника
- **Mandatory Code Protocol** — production-ready код с защитой от багов, memory management
- **Physics/Math Code Protocol** — документирование приближений, численная устойчивость
- **MoE Protocol** — 6-фазный анализ сложных задач с декомпозицией и red teaming
- **Hard-Engineering** — zero-allocation, real-time, eBPF, криптография, оптика
- **Memory & Context** — User Profile, History Retriever с автоматической активацией

## Что нового в v10.6

- **DEFAULT COMPLEX rule** — автоматическая сложная классификация при наличии кода/расчётов/архитектуры
- **Auto Memory Activation** — триггеры для History Retriever (упоминание проектов, людей, работы)
- **Always Protocol** — применение протоколов даже в простых задачах
- **Language Lock** — запрет переключения языка в ответе
- **No Emoji** — запрет бессмысленных эмодзи
- **Memory Retrieval Check** — механическая проверка использования памяти
- **Language Lock Check** — механическая проверка языка ответа

## Использование

Скопируйте `qwen_prompt.md` в system prompt вашего Qwen-приложения.

## Лицензия

MIT
