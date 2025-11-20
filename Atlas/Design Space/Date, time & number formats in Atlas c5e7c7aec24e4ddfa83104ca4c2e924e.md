# Date, time & number formats in Atlas

In Atlas, date, time, and number formatting are derived from the current app language. Because, as of the time of writing this article, Atlas is only available in English (UK), the formatting of dates, times and numbers should match what's commonly used in the UK.

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

[Date and time notation in the United Kingdom - Wikipedia](https://en.wikipedia.org/wiki/Date_and_time_notation_in_the_United_Kingdom)

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

Both the 24-hour and 12-hour notations are used in the UK. In Atlas, 24-hour clock is used.

---

# Date & time

## Format

```jsx
d mmm yyyy at 24-hour clock
```

## Example

```jsx
11 Nov 2021 at 19:58
```

In Atlas, when date & time are displayed together, separated by the “at” keyword, with no interpunction mark in-between.

---

# Time duration

In Atlas, to present a time duration:

- if possible use the extended format of time duration eg:

```jsx
12h 24m 43s
```

- if there is not enough space use the short format instead:

```jsx
12:24:43
```

If you are using short format presented above - remember to use 00 for hours if the time duration is less than 1 hour.

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

## General rules

In Atlas:

- numbers are displayed using **latin script,**
- space  `` is used as the **thousands separator**,
- period `.` is used as the **decimal separator**,
- negative values are displayed with a **negative sign at the beginning of the number**.

Further reading:

[Decimal separator - Wikipedia](https://en.wikipedia.org/wiki/Decimal_separator)

## Abbreviating large numbers

In Atlas, all numbers (such as the number of video views, or the price of an NFT) larger than 999 should be abbreviated whenever possible, based on the below conversion table:

| Value | Abbreviated value |
| --- | --- |
| 150.00 | 150 |
| 1 500.00 | 1.5K |
| 1 500 000.00 | 1.5M |
| 1 500 000 000.00 | 1.5B |
| 1 500 000 000 000.00 | 1.5T |
| 1 500 000 000 000 000.00 | 1 500T |

When displaying abbreviated numbers, it's critical to ensure there's a view or a page in the app that allows the user to see the full value. For example:

- NFT prices can be abbreviated in listing views, but the user should be able to see the full price when finalizing the transaction,
- The number of video views can be abbreviated in listing views, but the user should be able to see the full value on the video page.

Additionally, whenever there's an abbreviated number used, the user should be able to see the tooltip with the full value:

- On desktop devices, by hovering over the number with a cursor for at least one second,
- On touch devices, by tapping on the number (the tooltip should be dismissed automatically after 4 seconds, or by tapping on it).

[[Archived] Date, time & number formats in Atlas](Date,%20time%20&%20number%20formats%20in%20Atlas/%5BArchived%5D%20Date,%20time%20&%20number%20formats%20in%20Atlas%204441342b350d4a249f4c754773ee8ba0.md)