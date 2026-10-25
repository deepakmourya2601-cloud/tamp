# TAMP

[![GitHub repo size](https://img.shields.io/github/repo-size/sekedus/tamp?label=Size)](https://github.com/sekedus/tamp) [![GitHub Clones](https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count&url=https://gist.githubusercontent.com/sekedus/0f5fd62474258fa66560be80b6bf9904/raw/clone.json)](https://github.com/MShawon/github-clone-count-badge) [![GitHub License](https://img.shields.io/github/license/sekedus/tamp?label=License)](https://github.com/sekedus/tamp/blob/main/LICENSE)

TAMP (Termux, Apache, MariaDB, PHP)

TAMP is a local http web server for Android using Termux, with installation packages: Apache, MySQL/MariaDB, PHP, phpMyAdmin, & Composer.

ㅤ
## Requirements

- [Termux](https://github.com/termux/termux-app/releases/latest) **v0.118.0** or higher
- Stable and fast internet connection

ㅤ
## Installation

1. Install & open Termux
2. Update & upgrade packages: 
```bash
pkg update && pkg upgrade
```
3. Grant Termux storage permission: 
```bash
termux-setup-storage
```
4. Install `git` & clone this repo: 
```bash
pkg install git -y && cd ~/ && git clone https://github.com/sekedus/tamp.git
```
5. Install TAMP: 
```bash
cd ~/tamp && bash setup && cd ~/
```
6. Wait until installation is complete.
7. Enjoy!

ㅤ
## Usage

- Run `tamp start` to open url in browser.
- Local web server with SSL:
  * run: `tamp start-ssl`
  * port: `8443`
  * url: `https://localhost:8443`
- Login phpMyAdmin:
  * url: `http://localhost:8080/phpmyadmin`
  * username: `root`
  * password: {leave_it_blank}
- **htdocs** folder can be found in:
  * `/sdcard/htdocs`
  * or `/storage/emulated/0/htdocs`

ㅤ
## Commands

- tamp start
- tamp start-ssl
- tamp stop
- tamp update
- tamp uninstall

ㅤ
## Credits

- [Termux](https://github.com/termux/termux-app)
- [parzibyte.me](https://parzibyte.me/blog/en/2019/04/28/install-apache-php-7-android-termux/)
- [termux-php-apache2-setup](https://github.com/gungunpriatna/termux-php-apache2-setup)
- [termux-webserver](https://github.com/HadiKhoirudin/termux-webserver)

ㅤ
## License

TAMP is licensed under the GNU General Public License v3.0. See the [LICENSE](https://github.com/sekedus/tamp/blob/maiCREATE DATABASE reading_db
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;

USE reading_db;

CREATE TABLE admins (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(50) NOT NULL UNIQUE,
  password_hash VARCHAR(255) NOT NULL
);

CREATE TABLE readings (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(100) NOT NULL,
  reading_value VARCHAR(100) NOT NULL,
  reading_date DATE NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
n/LICENSE) file for more details.
