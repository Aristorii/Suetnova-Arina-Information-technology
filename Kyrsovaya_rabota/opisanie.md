# Описание работы · ТЗ № Т3-12/2026 · «Сахарный цех»

**Исполнитель:** [Суетнова Арина Евгеньевна], группа [11/1 рпо 26/1]

**Сайт:** https://tz-12-konditerskaya-saharnyy-ceh.vercel.app

**Период проверок:** [08.10] — [28.10]

## 1. Задача заказчика

Кондитерская «Сахарный цех» выполняет около 450 заказов в месяц, средний чек торта — 6 800 ₽. В сентябре 2026 года 37 заказов пришлось переделывать из-за ошибок в переписке: неверная начинка, дата или надпись. Компания не знает, какие публикации приводят заказы. Задача — сайт с конструктором торта, таблица заявок с источником и статусом, аналитика по каналам.

## 2. Схема работы

![Схема работы](docs/scheme.png)

Посетитель приходит из соцсетей или по QR-коду по ссылке с UTM-метками. Сайт отправляет события в GA4, а заявку — в Google Таблицу через Apps Script. Данные GA4 и таблицы собираются на дашборде DataLens.

## 3. Сайт

Сайт из 8 страниц создан с помощью [ChatGPT/Claude — укажи свой инструмент] и доработан вручную: тексты, адаптивность, форма. Опубликован на Vercel, обновляется после каждого push.

<img width="643" height="330" alt="glavnya" src="https://github.com/user-attachments/assets/da744da5-4b5b-427c-aa78-aaf22011ff0f" />

<img width="945" height="1280" alt="photo_5411552093547469896_y (1)" src="https://github.com/user-attachments/assets/13585074-771e-4043-bef4-353382fdc77c" />

<img width="588" height="1280" alt="photo_5411552093547469860_y" src="https://github.com/user-attachments/assets/86115cd4-0bce-454b-bd90-9fe2b75bdecc" />

## 4. Аналитика GA4

Настроено 18 событий, из них своих — 12. Ключевые события: `generate_lead`, `contact_click`, `messenger_click`. Каждое событие проверено в DebugView.

<img width="531" height="255" alt="karta" src="https://github.com/user-attachments/assets/adbd327c-9e1f-4bf1-b155-819f7236b1b2" />


## 5. UTM-ссылки и соцсети

В реестре 12 ссылок, размечены переходы из Instagram, ВКонтакте, Telegram, YouTube, у двух партнёров и на афише с QR-кодом.

<img width="1268" height="587" alt="Скриншот 29-10-2026 195410" src="https://github.com/user-attachments/assets/6a5b0aa6-2829-45a2-b137-24343cadf7c7" />

<img width="707" height="206" alt="salka" src="https://github.com/user-attachments/assets/4a3e1d57-7034-4c3c-96b3-674eb599d49a" />

## 6. Заявки

Форма отправляет заявку в Apps Script, тот проверяет поля и записывает строку в лист `leads` вместе с метками. Повторная отправка не создаёт дубль.

<img width="580" height="193" alt="Рисунок4" src="https://github.com/user-attachments/assets/2aa76ea7-9369-4980-a22e-95330f025991" />

<img width="488" height="246" alt="Рисунок5" src="https://github.com/user-attachments/assets/8c8259dc-458b-4d34-9ca7-16a923f3f756" />


## 7. Автоответы в Instagram

Комментарий «ГОСТИ» под Reel запускает ответ в комментариях и сообщение в Direct с кнопкой на сайт. Вторая ветка — слово «ДЕТИ».

<img width="1206" height="429" alt="photo_5411552093547469961_y (1)" src="https://github.com/user-attachments/assets/ce2e0f07-228f-4793-a1cf-fc80c4ca62f0" />

<img width="1203" height="780" alt="photo_5411552093547469954_y (1)" src="https://github.com/user-attachments/assets/ea0b1768-2f61-4776-9da1-d357c9ad96e7" />

## 8. Отчёты и дашборд

На дашборде DataLens собраны заявки по статусам. В GA4 настроены отчёты по источникам трафика.

<img width="568" height="450" alt="Рисунок6" src="https://github.com/user-attachments/assets/1ce6f0bb-7dad-4e5a-a90e-d4603a3b7083" />

## 9. Что получил бизнес

| **Было** | **Стало** |
|---|---|
| заказы в переписке Instagram и Telegram | все заявки в одной таблице со статусом |
| источник клиента неизвестен | у каждой заявки есть source, medium, campaign |
| бюджет делится «по ощущениям» | на дашборде видно заявки по каждому каналу |
| ответы на комментарии вручную | ManyChat отвечает сразу и ведёт на сайт |

## 10. Итог

**Не получилось:** подключить Google Sheets к DataLens напрямую, сработал только импорт CSV.

**ИИ использовался для:** вёрстки сайта, кода Apps Script.
