# GRaf-NEET AyuGramDesktop fork

This repository tracks [AyuGram/AyuGramDesktop](https://github.com/AyuGram/AyuGramDesktop) and carries one custom feature: keyboard navigation between the current user's editable messages in the active chat.

## Keyboard shortcuts

- `Alt+Shift+Up` starts editing the newest eligible outgoing message, or moves to the previous eligible message while editing.
- `Alt+Shift+Down` moves to the next eligible outgoing message while editing.

Navigation uses AyuGram's existing edit eligibility checks, skips messages that cannot be edited, and stops at the beginning or end of the available history.

## Branches and updates

- `dev` is a clean mirror of `AyuGram/AyuGramDesktop:dev`.
- `custom/edit-message-navigation` contains the custom patch and maintenance files.
- `.github/workflows/sync-upstream.yml` updates `dev` daily and rebases the custom branch. A conflict fails the workflow and requires a manual rebase.

## Releases

Custom releases use tags such as `v7.2.9-custom.1`, where `7.2.9` is the corresponding AyuGram version and the final number is the custom revision.

Unless a release explicitly includes platform packages, GitHub provides source archives only. Follow the upstream build documentation to produce binaries locally.

---

# Форк AyuGramDesktop от GRaf-NEET

Репозиторий следует за [AyuGram/AyuGramDesktop](https://github.com/AyuGram/AyuGramDesktop) и добавляет навигацию по собственным сообщениям, которые ещё можно редактировать.

- `Alt+Shift+Up` открывает последнее подходящее исходящее сообщение или переходит к предыдущему во время редактирования.
- `Alt+Shift+Down` переходит к следующему подходящему сообщению во время редактирования.
- Ветка `dev` остаётся чистой копией upstream.
- Ветка `custom/edit-message-navigation` содержит пользовательскую функцию и автоматически перебазируется на свежую `dev`.
- Если upstream конфликтует с патчем, автоматическое обновление завершается ошибкой и требует ручного rebase.

Если в Release не приложены пакеты для конкретной платформы, этот Release содержит только архивы исходного кода GitHub.
