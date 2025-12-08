# ESFSM Suite - Field Service Management for Odoo 18

Комплетен систем за управување со теренски сервис (Field Service Management) за Odoo 18.

## Модули

| Модул | Опис | Зависности |
|-------|------|------------|
| **esfsm** | Core FSM - работи, тимови, фази, чеклисти, потписи | base, hr, mail |
| **esfsm_stock** | Материјали и возила - следење на залиха по возило | esfsm, stock, fleet |
| **esfsm_project** | Проект интеграција - поврзување со project.task | esfsm, project |
| **esfsm_timesheet** | Времиња - евидентирање работни часови | esfsm, hr_timesheet |
| **esfsm_report** | Извештаи - PDF работен налог | esfsm |
| **esfsm_fleet** | Fleet интеграција - патувања и трошоци | esfsm, fleet |
| **esfsm_gallery** | Галерија - слики пред/после за работи | esfsm |
| **esfsm_api** | REST API - мобилна интеграција | esfsm |
| **esfsm_dashboard** | Dashboard - контролна табла | esfsm |
| **esfsm_viber** | Viber интеграција - нотификации | esfsm |

## Инсталација

### Клонирање со submodules

```bash
git clone --recurse-submodules https://github.com/Palifra/esfsm-suite.git
```

### Ако веќе е клониран

```bash
git submodule update --init --recursive
```

### Ажурирање на сите submodules

```bash
git submodule update --remote --merge
```

## Конфигурација на Odoo

Додајте ја патеката до `esfsm-suite` во `addons_path`:

```conf
[options]
addons_path = /path/to/odoo/addons,/path/to/esfsm-suite
```

## Минимална инсталација

За основна FSM функционалност, инсталирајте:

1. `esfsm` - Core модул (задолжителен)
2. `esfsm_stock` - За следење материјали
3. `esfsm_report` - За PDF извештаи

## Архитектура

```
esfsm-suite/
├── esfsm/              # Core FSM
├── esfsm_stock/        # Stock + Fleet интеграција
├── esfsm_project/      # Project интеграција
├── esfsm_timesheet/    # Timesheet интеграција
├── esfsm_report/       # PDF Reports
├── esfsm_fleet/        # Fleet детали
├── esfsm_gallery/      # Слики/галерија
├── esfsm_api/          # REST API
├── esfsm_dashboard/    # Dashboard
└── esfsm_viber/        # Viber нотификации
```

## Развој

### Работа со submodules

```bash
# Ажурирај специфичен submodule
cd esfsm
git pull origin main

# Комитирај промена на submodule pointer
cd ..
git add esfsm
git commit -m "Update esfsm submodule"
```

### Клонирање за развој

```bash
# Со SSH (за contributors)
git clone --recurse-submodules git@github.com:Palifra/esfsm-suite.git
```

## Лиценца

LGPL-3.0

## Автор

**ЕСКОН-ИНЖЕНЕРИНГ ДООЕЛ Струмица**
- Website: https://www.eskon.com.mk
- Email: info@eskon.com.mk
- GitHub: https://github.com/Palifra
