# Link Checker

Перевірка розміщених посилань.

Коли сторінка перестає відповідати, це ще не означає, що з неї прибрали посилання. Link Checker розрізняє ці випадки, щоб SEO-фахівець знав, де потрібна повторна перевірка.

Інструмент перевіряє, чи є на сторінці очікуване посилання, чи веде воно прямо на потрібну адресу та чи має атрибут `nofollow`. Результат можна переглядати в таблиці.

## English overview

A page that fails to load needs a different follow-up from a page that loads correctly but no longer links to its target. Link Checker distinguishes those cases and reports whether a link is direct and whether it carries a `nofollow` attribute.

### Ілюстративний фрагмент

Спрощений приклад показує різницю між відсутнім посиланням і невдалою перевіркою. Вхідні значення вигадані.

```python
def review_label(page_loaded, target_found):
    if not page_loaded:
        return "check_again"
    if target_found:
        return "found"
    return "missing"

assert review_label(False, False) == "check_again"
assert review_label(True, False) == "missing"
```

[До каталогу інструментів](README.md)
