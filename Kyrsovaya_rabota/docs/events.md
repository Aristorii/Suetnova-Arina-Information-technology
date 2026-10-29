# События GA4 — «Сахарный цех»

| № | Событие | Тип | Где отправляется | Параметры |
|---|---|---|---|---|
| 1 | page_view | авто | все страницы | page_location, page_title |
| 2 | scroll | авто | все страницы | percent_scrolled |
| 3 | click | авто | внешние ссылки | link_url, outbound |
| 4 | file_download | авто | PDF с сайта | file_name, file_extension |
| 5 | form_start | авто | contacts.html | form_id |
| 6 | form_submit | авто | contacts.html | form_id |
| 7 | generate_lead | своё | js/analytics.js | lead_cake_type, weight_kg, value, currency |
| 8 | cta_click | своё | все кнопки заявки | button_name, page_section |
| 9 | cake_filter | своё | cakes.html | occasion |
| 10 | view_item | своё | cakes.html, index.html | items, currency, value |
| 11 | cake_build | своё | builder.html | weight_kg, tiers, filling, total_price |
| 12 | filling_view | своё | fillings.html | filling_name |
| 13 | allergen_filter | своё | fillings.html | allergen |
| 14 | guests_calc | своё | guests.html | guests, weight_kg |
| 15 | contact_click | своё | contacts.html, index.html | contact_type |
| 16 | messenger_click | своё | contacts.html | messenger |
| 17 | social_click | своё | подвал, thanks.html | network, page_section |
| 18 | form_error | своё | js/form.js | field_name, error_type |

Пример значения: `cake_build` → `weight_kg=3, tiers=1, filling=chocolate, total_price=7800`.

Пользовательские параметры (Event scope): `button_name`, `page_section`, `occasion`, `filling`, `allergen`, `guests`, `messenger`.

Ключевые события: `generate_lead`, `contact_click`, `messenger_click`.
