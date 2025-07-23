# 🧠 XSS-MimeSploit by [adce626](https://github.com/adce626)

🎯 **The Ultimate Cross-Context XSS Payload Arsenal**

Welcome to **XSS-MimeSploit**, a powerful, context-aware repository created by `adce626` for offensive security researchers, bug bounty hunters, and XSS maniacs. This toolkit provides payloads tailored for various **MIME types** and **file formats**, designed to break filters, bypass WAFs, and trigger alerts where no alert should be.

> 🚨 Disclaimer: This project is strictly for educational purposes and authorized testing. Use responsibly.

---

## 🧩 Payload Categories

Organized by file format and exploitation context:

| Type       | Description                                    |
|------------|------------------------------------------------|
| `svg/`     | SVG-based inline script/onload/injection       |
| `pdf/`     | PDF JavaScript injection (`OpenAction`, etc.)  |
| `json/`    | Payloads in JSON keys, values, and nesting     |
| `xml/`     | XML entity injection / CDATA-based XSS         |
| `html/`    | Classic HTML tag injection (DOM & reflected)   |
| `js/`      | JS-context injection and eval bypasses         |
| `others/`  | Mixed/rare payloads (`xlsx`, `jsf`, `xul`, …)  |

---

## 🧪 Sample Payloads

### 🔸 SVG
```xml
<svg/onload=alert(1)>
<svg><script>alert('XSS')</script></svg>
<svg><a href="javascript:alert(1)">click</a></svg>
