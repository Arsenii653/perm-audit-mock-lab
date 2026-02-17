# CI report (GitHub Actions)

## 1) Что такое CI (своими словами)
CI (Continuous Integration) — это способ создания программного обеспечения, при которой разработчики регулярно интегрируют свои изменения в общий репозиторий. Каждый раз, когда происходит интеграция, специальные тесты запускаются автоматически. Это помогает выявлять и устранять ошибки на ранних этапах разработки, улучшая качество кода и ускоряя процесс разработки.

## 2) Что проверяет ваш workflow
- Мой workflow проверяет, что все тесты в проекте проходят успешно. 
- Он устанавливает Python 3.11, после устанавливает необходимые пакеты (pytest) и запускает тесты. Если все тесты проходят, workflow считается успешным; если какой-либо тест не проходит, workflow будет красным, указывая на наличие проблем в коде.

## 3) Ссылка на PR
https://github.com/Arsenii653/perm-audit-mock-lab/pull/1

## 4) Что было красным и как вы починили
- Красным было из-за того, что в проекте не было установки pytest, и тесты просто не могли запуститься. Я исправил это, добавив шаг в workflow с установкой pytest перед самими тестами. Теперь все тесты проходят успешно, и workflow зеленый.

## 5) Команды
Вставь вывод:
- python -m pytest -q
    PS C:\17-02-2026\ci_actions_lab_starter\ci_actions_lab> python -m pytest -q  
    ..                                                              [100%]
    2 passed in 0.02s
    PS C:\17-02-2026\ci_actions_lab_starter\ci_actions_lab> 

- git log --oneline --decorate --graph --all
    ~
    ~
    (END)...skipping...
    *   99dc1b8 (HEAD -> main, tag: v0.4, origin/main, origin/HEAD) Merge branch 'ci/actions'
    |\
    | * bda4102 (origin/ci/actions, ci/actions) fix: install pytaest in CI 
    | * cc2a27f fix: install pytaest in CI
    | * f107f35 fix: install pytaest in CI
    * | 964d409 Remove comments from tests workflow
    * | 80978d6 Merge pull request #1 from Arsenii653/ci/actions
    |\|
    | * ec3e8e4 CI: add GitHub actions to run pytest
    |/
    * e6ae712 initial

- git tag
    PS C:\17-02-2026\ci_actions_lab_starter\ci_actions_lab> git tag
    v0.4

## 6) AI usage
- Я использовал AI для поиска проблем в Action на GitHub, как потом оказалось проблема была в том что я смотрел на страый коммит, еще не исправленный, AI помого мне понять что я не туда смотрю и изначально код у меня правильный

