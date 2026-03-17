# Журнал изменений

Все заметные изменения в этом проекте будут задокументированы в этом файле.

Формат основан на [Keep a Changelog](https://keepachangelog.com/ru/1.0.0/),
и этот проект придерживается [Semantic Versioning](https://semver.org/lang/ru/).

## [1.0.2] - 2026-03-17

### Добавлено

- Первоначальный релиз расширения для 1С:Предприятие 8 с HTTP-сервисом и эндпоинтом `GET /metrics` в формате Prometheus Text Format.
- Хранение реестра метрик в справочнике `PrometheusХранилище` (через модуль `PrometheusRegistryStorage`) и встроенные метрики `app_up`, `metrics_requests_total`.
- Фасад `PrometheusFacade` для создания и использования метрик (счётчик, индикатор, гистограмма, резюме и векторы), совместимый по API с библиотекой `prometheus`.
- Пример проектного расширения `prometheus_project_example` с хелпером `PrometheusПроект_ТестМетрикХелпер`.
