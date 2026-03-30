# Журнал изменений

Все заметные изменения в этом проекте будут задокументированы в этом файле.

Формат основан на [Keep a Changelog](https://keepachangelog.com/ru/1.0.0/),
и этот проект придерживается [Semantic Versioning](https://semver.org/lang/ru/).

## [1.0.4] - 2026-03-30

### Изменено

- Реестр метрик в регистре сведений `PrometheusДанныеРеестра` (строка на коллектор); встроенные метрики
  `prometheus_client_up`, `prometheus_client_http_requests_total` с лейблом `handler="/metrics"`.

## [1.0.3] - 2026-03-24

### Изменено

- Изменён режим совместимости основной конфигурации на Version8_3_27
- Изменён режим совместимости расширений на Version8_3_20
- Удалены пустые модули ManagedApplicationModule и SessionModule в расширении prometheus_client
- Удалён DefaultLanguage в расширении prometheus_client и prometheus_project_example

## [1.0.2] - 2026-03-17

### Добавлено

- Первоначальный релиз расширения для 1С:Предприятие 8 с HTTP-сервисом и эндпоинтом `GET /metrics` в формате Prometheus Text Format.
- Хранение реестра метрик в справочнике `PrometheusХранилище` (через модуль `PrometheusRegistryStorage`) и встроенные метрики `app_up`, `metrics_requests_total`.
- Фасад `PrometheusFacade` для создания и использования метрик (счётчик, индикатор, гистограмма, резюме и векторы), совместимый по API с библиотекой `prometheus`.
- Пример проектного расширения `prometheus_project_example` с хелпером `PrometheusПроект_ТестМетрикХелпер`.
