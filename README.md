# qrscan-privacy

Політика конфіденційності застосунку **QR Scan & Share** на GitHub Pages:
<https://airstep.github.io/qrscan-privacy/>

| Де використовується | |
|---|---|
| App Store Connect → App Privacy → Privacy Policy URL | iOS `pro.bearer.qrscan` |
| Play Console → Policy → App content → Privacy policy | Android `com.tgs.qrscanner` |
| AdMob → Конфіденційність і повідомлення → повідомлення GDPR / США | посилання на політику у формі згоди |

Сторінка самодостатня: один `index.html`, перемикач EN / UK на клієнті
(`#uk` у URL відкриває українську одразу), шрифти з Google Fonts. Збірки немає.

## URL заморожений

Адреса потрапляє в обидва магазини й у форму згоди AdMob. Перейменування
репозиторію ламає URL.

## Що потребує правки й коли

Політика описує застосунок станом на редакцію 2: реклама Google AdMob з UMP,
rewarded «24 години без реклами», історія сканувань зберігається на пристрої
(до 500 записів), жодної аналітики й покупок. Оновити **до** релізу версії, яка це змінює:

| Подія | Що міняється |
|---|---|
| покупка Pro (`in_app_purchase`) | розділи 2, 3, 4: магазин обробляє оплату, застосунок зберігає статус покупки |
| Firebase Analytics / Crashlytics | розділи 2, 4, 9 + App Privacy / Data safety |
| медіація AdMob (AppLovin, Meta, Unity…) | розділ 2: перелік рекламних партнерів і посилання на їхні політики |
| сканування з галереї (`mobile_scanner`) | розділ 6: дозвіл на читання фото (або системний вибір фото) |

Дата (`effective`) і редакція оновлюються в шапці й футері обох мов разом із
текстом.

## Юридичний статус

Текст підготував AI-асистент. Це не юридична консультація; вичитка юристом —
на власникові.

## Публікація

```bash
git add -A && git commit -m "Update privacy policy" && git push
```

GitHub Pages: Settings → Pages → Source `Deploy from a branch`, гілка `main`,
тека `/ (root)`.
