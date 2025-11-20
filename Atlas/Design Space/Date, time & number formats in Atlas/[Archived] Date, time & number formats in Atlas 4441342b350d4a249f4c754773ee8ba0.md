# [Archived] Date, time & number formats in Atlas

<aside>
📆 Before 20 May, 2022

</aside>

Because as of the time of writing below guidelines majority of Atlas' user base is European, and because Atlas is available in English only, there is **one** format of dates & numbers used for all users, regardless of their locale.

---

# Date

## Format

```jsx
d mmm yyyy
```

## Example

```jsx
11 Nov 2021
```

In Atlas, the `DMY` (DAY, MONTH, YEAR) convention is used in `d mmm yyyy` format, where:

- `d` — one-digit day of the month for days below 10, *e.g. 2,*
- `mmm` — three-letter abbreviation for month, *e.g. Apr,*
- `yyyy` — four-digit year, *e.g. 2016.*

Further reading:

[Date format by country - Wikipedia](https://en.wikipedia.org/wiki/Date_format_by_country)

---

# Time

## Format

```jsx
24-hour clock
```

## Example

```jsx
19:58
```

In Atlas, 24-hour clock is used.

---

# Time duration

In Atlas to represent time duration:

- if possible use the extended format of time duration eg:

```jsx
12h 24m 43s
```

- if there is not enough space use the short format instead:

```jsx
12:24:43
```

If you are using short format presented above - remember to use 00 for hours if the time duration is less than 1 hour 

```jsx
00:24:43
```

---

# Relative timestamps

In Atlas, whenever a relative timestamp is displayed, the following convention should be used:

- `X seconds ago` if less than 60 seconds ago,
- `X minutes ago` if less than 60 minutes ago,
- `X hours ago` if less than 24 hours ago,
- `X days ago` if less than 7 days ago,
- `X weeks ago` if less than 30 days ago,
- `X months ago` if less than 365 days ago,
- `X years ago` if equal or more than 365 days ago.

Please note, that a singular form of a time unit name should be used when needed, eg. `1 week ago`

instead of `1 weeks ago`.

---

# Numbers

## European

```jsx
10 508,58 tJOY
```

## American

```jsx
10,508.58 tJOY
```

## General rules

In Atlas:

- numbers are displayed using **latin script,**
- space  `` is used as the **thousands separator**,
- comma `,` is used as the **decimal separator**,
- negative values are displayed with a **negative sign at the behinning of the number**.

Further reading:

[Decimal separator - Wikipedia](https://en.wikipedia.org/wiki/Decimal_separator)

## Abbreviating large numbers

In Atlas, all numbers (such as the number of video views, or the price of an NFT) larger than 999 should be abbreviated whenever possible, based on the below conversion table:

| Value | Abbreviated value |
| --- | --- |
| 150,00 | 150 |
| 1 500,00 | 1,5K |
| 1 500 000,00 | 1,5M |
| 1 500 000 000,00 | 1,5B |
| 1 500 000 000 000,00 | 1,5T |
| 1 500 000 000 000 000,00 | 1 500T |

When displaying abbreviated numbers, it's critical to ensure there's a view or a page in the app that allows the user to see the full value. For example:

- NFT prices can be abbreviated in listing views, but the user should be able to see the full price when finalizing the transaction,
- The number of video views can be abbreviated in listing views, but the user should be able to see the full value on the video page.

Additionally, whenever there's an abbreviated number used, the user should be able to see the tooltip with the full value:

- On desktop devices, by hovering over the number with a cursor for at least one second,
- On touch devices, by tapping on the number (the tooltip should be dismissed automatically after 4 seconds, or by tapping on it).