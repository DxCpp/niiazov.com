---
title: "Как установить Ansible в macOS"
date: 2024-11-24
description: ""
tags: ["Ansible", "Linux", "macOS"]
type: post
weight: 20
showTableOfContents: true
image: "1.png"
---
Самый простой способ установить и поддерживать Ansible в macOS — использовать Homebrew Package Manager. Он уже имеет сборку Ansible с несколькими доступными версиями. Главное преимущество использования brew в том, что он заботится обо всех необходимых зависимостях и также управляет процессом обновления. Альтернативой может быть использование Python PIP, но вам придется загружать исходный код и компилировать программное обеспечение. Это может быть решением для разработчика, который всегда хочет иметь последнюю актуальную версию.
## Демонстрационная установка Ansible в macOS
Позвольте мне объяснить вам, как установить последнюю и конкретную версию Ansible в macOS с помощью Homebrew Package Manager.

### Установим последнюю версию
```
#!/bin/bash
brew --version
brew search ansible
brew install ansible
ansible --version
```
### Установим определенную версию
```
#!/bin/bash
brew remove ansible
brew search ansible
brew install ansible@2.9
/usr/local/opt/ansible\@2.9/bin/ansible --version
```
## Проверка
После успешной установки вы можете проверить в командной строке:

```
% ansible --version
ansible [core 2.13.1]
  config file = None
  configured module search path = ['/Users/lberton/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/Cellar/ansible/6.1.0/libexec/lib/python3.10/site-packages/ansible
  ansible collection location = /Users/lberton/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/local/bin/ansible
  python version = 3.10.5 (main, Jun 23 2022, 17:15:32) [Clang 13.0.0 (clang-1300.0.29.30)]
  jinja version = 3.1.2
  libyaml = True
```

