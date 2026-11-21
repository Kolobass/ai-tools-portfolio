# Outreach Tool

Робота з поштовими кампаніями.

Коли кампанія використовує кілька поштових скриньок, команді потрібно бачити, які дії вже виконано і де сталася помилка. Я розробляв і підтримував інструмент для цієї роботи.

Журнал подій допомагав оператору відшукати проблемний крок і вирішити, що перевіряти далі. Це особливо важливо перед повторною дією, коли перше відправлення могло вже відбутися.

## English overview

I built and maintained a tool for a team running outreach campaigns across multiple mailboxes. I added logging so operators could trace a failure and check what had already happened before deciding whether to retry.

### Ілюстративний фрагмент

Приклад підраховує події, позначені для ручного перегляду. Усі значення вигадані.

```python
events = ["recorded", "needs_review", "recorded", "needs_review"]
review_count = sum(event == "needs_review" for event in events)
assert review_count == 2
```

[До каталогу інструментів](README.md)
