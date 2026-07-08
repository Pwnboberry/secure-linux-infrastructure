# Secure Linux Infrastructure

## 🎯 Цель проекта
Развертывание и защита корпоративной инфраструктуры на базе Linux.

## 🏗️ Архитектура
- Firewall на базе Linux (nftables)
- Domain Controller на Samba AD
- Клиенты: Windows 10/11

## 🔒 Реализованные меры безопасности
- SSH Hardening (запрет root, ключи, смена порта)
- Firewall nftables (разрешен только 22,53,443)
- Шифрование LUKS для /secure-data
- Аудит через auditd
- Резервное копирование

## 📂 Структура
- `/docs` - Документация
- `/network` - Сетевая топология
- `/samba-ad` - Настройка домена
- `/firewall` - Правила nftables
- `/ssh-hardening` - Безопасный SSH
- `/backup` - Скрипты бэкапа
- `/monitoring` - Мониторинг Zabbix
- `/scripts` - Скрипты автоматизации

## 🚀 Быстрый старт
```bash```
# Клонировать репозиторий
git clone https://github.com/username/secure-linux-infrastructure.git 

# Запустить создание пользователей
sudo ./scripts/user_create.sh users.txt

# Применить правила firewall
sudo nft -f firewall/nftables.conf
