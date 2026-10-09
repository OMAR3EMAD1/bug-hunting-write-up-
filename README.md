# bug-hunting-write-up-
this is write up of vuln i found in a real website .

| **نوع الثغرة** | Missing Security Header (CSP) |
| **OWASP Category** | A05:2021 - Security Misconfiguration |
| **CWE** | CWE-693: Protection Mechanism Failure |

while my researche i found a security header missing in this website (content security policy (csp))
Without this header, the browser trusts any An external source is loading resources, allowing attackers to steal sessions and launch attacks such as click

poc :

<!DOCTYPE html>
<html>
<body>
  <h1>Test For Clickjacking</h1>
  <iframe src="https://examble.com/" width="800" height="600"></iframe>
</body>
</html>
