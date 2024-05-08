## w9scan

> An all-round website vulnerability scanner that draws on the excellent codes of its predecessors. The built-in 1200+ plug-ins can conduct a large-scale detection of the website. The functions include but are not limited to web fingerprint detection, port fingerprint detection, website structure analysis, various popular vulnerability detection, crawler and SQL injection detection, XSS detection, etc. w9scan will Automatically generate beautiful HTML format result reports.

[![Python 2.7](https://img.shields.io/badge/python-2.7-yellow.svg)](https://www.python.org/) [![License](https://img.shields.io/badge/license-GPLv2-red.svg)](https://github.com/boy-hack/w9scan/blob/master/GPL-2.0)

#### Target

- Universal for Linux/Windos
- Python 2 does not require additional installation of third-party libraries
- Be the Top 1 open source scanner
- Let the software work first, and then optimize various details
- [Version upgrade record](./UPDATELOG.MD)

###Usage

- `python w9scan.py --update` updater
- `python w9scan.py --guide` starts w9scan in wizard mode
- `python w9scan.py -u "https://x.hacking8.com" ` Quickly scan the website
- `python w9scan.py -u "https://blog.hacking8.com/" -p emlog` specifies the plugin to scan the website
- `python w9scan.py -u "@1.txt" -p emlog` specifies the plug-in to scan websites in batches
- `python w9scan.py -s emlog` Search whether the plug-in exists
- `--banner` output banner
- `--debug` output debugging information

[![asciicast](https://asciinema.org/a/4WhO54hcf43fySjxJOLyjczSm.png)](https://asciinema.org/a/4WhO54hcf43fySjxJOLyjczSm)

#### TIPS

- I don’t believe in the command line philosophy. I’ll keep it as simple as possible.
- Directly use `python w9scan.py` to use w9scan in wizard mode
- When entering URL in wizard mode, you can enter something like `@1.txt`, which means batch scanning of URLs in 1.txt
- For configuration thread, timeout, header and other parameters, you can open config.conf configuration
- Use the `-u` parameter to load the `fingerprint recognition` `service discovery` module by default, and disable `fuzz` `subdomain name blasting`, etc.

## Features

- **Fingerprint Detection**

  - Can identify common website CMS fingerprints (`300`+)
  - Can identify common website frames Frame
  - Identify common port service fingerprints
  - Detect website script language
    - Detect operating system type
  - Detect website firewalls (WAF)

- **Attack Parameters**

  - SQL injection (crawler-based)
    - XSS injection (crawler-based)
    - A large number of Fuzz parameter scans
    - CVE vulnerability
    - `1200+` Specifies plug-in directional verification attacks. For plug-in support, please refer to [https://github.com/boy-hack/w9scan/tree/master/plugins](https://github.com/boy-hack/w9scan/ tree/master/plugins)
    - `struts` vulnerability collection (including automatic detection)
    - Shellshock cgi test
    - `heartbeat` heart bleeding
    - IIS parsing vulnerability
    - IIS Put vulnerability

- **Brute force**

  - Backup files and directories (based on crawler)
  - Backup files and directories (based on domain name)
  - Common directories
  - Common documents
    - Violent resolution of subdomain names
    - `fckeditor` path enumeration
    - Common `mdb` database enumeration
    - `git` `svn` leak identification
    - `TOMCAT web.xml` leaked

- **collect message**
  - Emails (crawler-based)
  - Private IP (crawler based)
  - E-mail (based on crawler)
  - Detect Warnings, Fatal Error,...
    - PHP version identification
    - IIS information leakage
    - IP address ownership
    - Integrated `Wappalyzer` recognition script
    - `robots.txt` parsing
    - Detect unsafe headers in headers
    - Detect insecure factors in cookies

## FAQ

- Compatible with bugscan plug-in?
  The program design is run by calling the bugscan plug-in. The bugscan plug-ins are all collected online.
- Is the plug-in built-in?
  Built-in 1300+ plug-ins, constantly updated
- How to communicate?
  You can email or open an issue. If you want to study the code, you can refer to the following article.
  1. [http://www.freebuf.com/sectool/162120.html](http://www.freebuf.com/sectool/162120.html)
  2. [https://blog.hacking8.com/?tag=w9scan](https://blog.hacking8.com/?tag=w9scan)

## Disclaimer

The w9scan scanner project is only used for learning and self-checking network security, and other uses are prohibited.

## Thx

- Partial reference for the crawler's SQL and XSS modules [https://github.com/youmengxuefei/web_vul_scan](https://github.com/youmengxuefei/web_vul_scan)
- Modeled after [POC-T](https://github.com/Xyntax/POC-T/) code structure
- Network access engine [Hackhttp](https://github.com/BugScanTeam/hackhttp/)
- Crawler-based backup file search [bcrpscan](https://github.com/secfree/bcrpscan)
- [WebEye](https://github.com/zerokeeper/WebEye/)
- [cobra](https://github.com/wufeifei/cobra)
- [s7scan](https://github.com/jiangsir404/S7scan)
- [WAScan](https://github.com/m4ll0k/WAScan)
- [ctf-wscan](https://github.com/kingkaki/ctf-wscan)
