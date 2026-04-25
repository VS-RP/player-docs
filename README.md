# VS:RP — Player & Support Docs

Источник документации VS:RP. Сборка статического сайта — [MkDocs Material](https://squidfunk.github.io/mkdocs-material/), деплой в GitHub Pages через GitHub Actions.

## Структура

```
docs/
  index.md              # титульная страница
  events-guide.md       # игровые события
  player/               # документация для игроков
  support/              # документация для специалистов поддержки
mkdocs.yml              # конфиг сайта (тема, навигация, расширения)
.github/workflows/      # workflow деплоя в GitHub Pages
```

## Локальный просмотр

```bash
python -m venv .venv
.venv/Scripts/activate    # Windows; на Linux/macOS: source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve              # http://127.0.0.1:8000
```

## Деплой

Любой push в `master` запускает workflow `Deploy docs to GitHub Pages`. После первого запуска включить Pages: **Settings → Pages → Source = GitHub Actions**.

## Использование как submodule

Этот репозиторий подключён к серверу VS:RP в `src/Docs` как git submodule. Правки делаются здесь; в серверном репозитории обновляется указатель коммита.
