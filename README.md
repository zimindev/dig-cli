# 🌐 dig — DNS Query Utility

**dig** (Domain Information Groper) is a powerful command-line tool for querying DNS (Domain Name System) servers. It's commonly used for troubleshooting DNS issues and retrieving DNS records of domains.

---

## ✅ Features

- Query A, AAAA, MX, NS, TXT, SOA, and other DNS records
- Check specific DNS servers
- Debug and diagnose DNS problems
- Scriptable and widely available

---

## 🔧 Installation

### Debian/Ubuntu
```bash
sudo apt install dnsutils
```

### Arch Linux
```bash
sudo pacman -S bind
```

### Fedora
```bash
sudo dnf install bind-utils
```

---

## 🚀 Basic Usage

### Lookup A record (IPv4 address)
```bash
dig example.com
```

### Lookup AAAA record (IPv6 address)
```bash
dig example.com AAAA
```

### Lookup MX records (mail servers)
```bash
dig example.com MX
```

### Use a specific DNS server
```bash
dig @8.8.8.8 example.com
```

### Get only the answer section
```bash
dig +short example.com
```

### Query all available records
```bash
dig example.com ANY
```

---

## 🧾 Output Sections

- **HEADER**: Info about the query
- **QUESTION SECTION**: What you asked
- **ANSWER SECTION**: DNS records returned
- **AUTHORITY SECTION**: Info about authoritative name servers
- **ADDITIONAL SECTION**: Extra information like IPs of name servers

---

## 🧩 Tips

- Great for DNS debugging and checking propagation
- Use `+trace` to follow DNS resolution from root
  ```bash
  dig +trace example.com
  ```
- Combine with `watch` to check changes over time:
  ```bash
  watch -n 5 "dig +short example.com"
  ```

---

## 📚 More Info

- Run `man dig` for the full manual
- Official page: [https://man7.org/linux/man-pages/man1/dig.1.html](https://man7.org/linux/man-pages/man1/dig.1.html)
