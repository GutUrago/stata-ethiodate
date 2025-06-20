
# ethiodate: Ethiopian Date Conversion Utilities for Stata

![version](https://img.shields.io/badge/version-1.0.0-blue)
[![Stata](https://img.shields.io/badge/Stata-ado-blue.svg)](https://www.stata.com)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](./LICENSE)

The ***ethiodate*** package offers a fast, reliable, and user-friendly solution for converting dates between the Gregorian and Ethiopian calendar systems directly within Stata. Built in Mata for maximum computational efficiency, it provides super-fast date conversions.

---

## 🚀 Installation

You can install or update the latest version of **ethiodate** directly from GitHub using:

```stata
net install ethiodate, from("https://raw.githubusercontent.com/GutUrago/stata-ethiodate/main/") replace
```

This will download and install all necessary files.

---

## 📦 Available Commands

### `to_gregorian`
Converts Ethiopian calendar date variables (year, month, day) to a single Gregorian Stata date.

```stata
to_gregorian eth_year eth_month eth_day, gre_date(newvar)
```

- `eth_year`, `eth_month`, and `eth_day`: numeric variables with Ethiopian date components.
- `gre_date()`: name of the new Gregorian Stata date variable to create.

**Example:**

```stata
to_gregorian eth_yr eth_mo eth_dy, gre_date(greg_date)
```

### `to_ethiopian`
Converts Gregorian calendar date variable to Ethiopian date components: year, month, day.

```stata
to_ethiopian gre_date, eth_year(newvar) eth_month(newvar) eth_day(newvar)
```

- `eth_year`, `eth_month`, and `eth_day`: new numeric variables name of Ethiopian date components.
- `gre_date()`: name of the Gregorian Stata date variable to convert.

**Example:**

```stata
to_gregorian eth_yr eth_mo eth_dy, gre_date(greg_date)
to_ethiopian greg_date
```

---

## 📖 Help

To get detailed documentation in Stata, type:

```stata
help ethiodate
help to_gregorian
help to_ethiopian
```


## 📌 Features

- Fully vectorized, efficient and precise date conversion
- Supports use within data cleaning and transformation pipelines
- Compatible with Stata 10.0 and later
- Clear help files and user instructions

---

## 👨‍💻 Author

**Gutama Girja Urago**  
Research Analyst at Laterite Consulting PLC 

[LinkedIn](https://www.linkedin.com/in/gutama-girja/) | [GitHub](https://github.com/GutUrago)

---

## 🛠 Contributing

Contributions, feedback, and issue reports are welcome! Please open a pull request or submit an issue via the [GitHub repository](https://github.com/GutUrago/stata-ethiodate).
