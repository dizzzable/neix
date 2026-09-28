# Privacy policy / Политика конфиденциальности

NEIX has no telemetry, no analytics, no accounts and no servers of its own. Your
subscriptions, servers, keys, settings and connection history stay on your device,
encrypted. The program connects only to the places listed below.

## What NEIX connects to

| Where | When | What is sent |
|---|---|---|
| The VPN servers and subscription addresses **you** add | when you connect, ping servers or refresh subscriptions (and on the refresh interval you set) | what the protocol needs; for subscriptions an HTTP request with NEIX's User-Agent (or the one you set) and the device headers subscription panels count devices by (a random device ID made by NEIX, the OS and model) — on by default, off with “Send HWID” |
| `api.github.com`, `github.com` (this project's releases) | twice a day while “Check for updates automatically” is on (you can turn it off); the download only when you press “Update” | an ordinary HTTPS request with `NEIX/<version>` as User-Agent |
| `github.com`, `cdn.jsdelivr.net` (the roscomvpn and runetfreedom geo databases) | when routing needs them and when they are out of date | an ordinary HTTPS request |
| `www.gstatic.com/generate_204` (or the address you set) | while connected, through the VPN: whether traffic passes | an empty request |
| `1.1.1.1`, `8.8.8.8` (DNS over HTTPS) | only when a subscription, update or geo host cannot be resolved the usual way | the host name |
| `ya.ru`, `vk.com`, `www.gosuslugi.ru`, `www.google.com`, `www.cloudflare.com` | only when the connection fails: whether the network lets through only approved sites (“white lists”) | ordinary HTTPS requests |
| `www.cloudflare.com/cdn-cgi/trace`, `speed.cloudflare.com` | only when you press “Check IP and leaks”, run diagnostics or a speed test | ordinary HTTPS requests |

Nothing else: no crash reports, no usage statistics. A diagnostic report is written to a
file only when you ask for one, with keys, UUIDs and addresses removed; you decide whether
to send it to anyone.

---

NEIX не собирает телеметрию и статистику, не требует аккаунтов, у проекта нет своих
серверов. Подписки, серверы, ключи, настройки и история подключений хранятся на устройстве в
зашифрованном виде. Программа обращается только туда, куда указано в таблице выше: к вашим
серверам и подпискам (с заголовками устройства для панелей — случайный ID, ОС и модель;
выключается «Отправлять HWID»), к GitHub за
обновлениями (два раза в день, если включена автопроверка; скачивание — только по кнопке
«Обновить»), к GitHub и jsDelivr за геобазами, к `generate_204` через VPN (проходит ли
трафик), к DoH Cloudflare/Google — только если адрес не разрешился обычным путём, к нескольким
сайтам — только когда подключение не работает (проверка «белых списков»), и к Cloudflare —
только по вашей кнопке (проверка IP, диагностика, замер скорости). Отчёт для обращений
сохраняется в файл только по запросу и без ключей, UUID и адресов.
