# VS Code Keybindings

Zestaw przydatnych skrótów klawiszowych dla Visual Studio Code usprawniających pracę z terminalem, nawigację w projekcie oraz edycję i refaktoryzację kodu.

---

## ⌨️ Zestawienie skrótów

### 💻 Terminal i przełączanie fokusu

| Skrót | Polecenie | Działanie | Warunek (`when`) |
| :--- | :--- | :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>`</kbd> | `workbench.action.terminal.toggleTerminal` | Pokazuje lub ukrywa dolny panel zintegrowanego terminala | — |
| <kbd>Alt</kbd> + <kbd>J</kbd> | `workbench.action.terminal.focus` | Przenosi fokus z edytora kodu do wnętrza terminala | `!terminalFocus` |
| <kbd>Alt</kbd> + <kbd>K</kbd> | `workbench.action.focusActiveEditorGroup` | Przenosi kursor z wnętrza terminala z powrotem do aktywnego pliku | `terminalFocus` |

### 🧭 Nawigacja po kodzie i plikach

| Skrót | Polecenie | Działanie | Warunek (`when`) |
| :--- | :--- | :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>P</kbd> | `workbench.action.quickOpen` | Otwiera menu szybkiego wyszukiwania plików po nazwie | — |
| <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> | `workbench.action.showCommands` | Otwiera Paletę Poleceń z dostępem do wszystkich funkcji | — |
| <kbd>Ctrl</kbd> + <kbd>T</kbd> | `workbench.action.showAllSymbols` | Przeszukuje symbole, klasy i metody w całym projekcie | — |
| <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>O</kbd> | `workbench.action.gotoSymbol` | Wyszukuje metody, funkcje i pola wewnątrz bieżącego pliku | — |
| <kbd>F12</kbd> | `editor.action.revealDefinition` | Skacze bezpośrednio do definicji lub deklaracji elementu | `editorHasDefinitionProvider && editorTextFocus && !isInEmbeddedEditor` |
| <kbd>Shift</kbd> + <kbd>F12</kbd> | `editor.action.goToReferences` | Wyświetla okno ze wszystkimi wywołaniami danej metody | `editorHasReferenceProvider && editorTextFocus && !inReferenceSearchEditor && !isInEmbeddedEditor` |
| <kbd>Alt</kbd> + <kbd>F12</kbd> | `editor.action.peekDefinition` | Szybki podgląd definicji w małym oknie bez opuszczania bieżącej linii | `editorHasDefinitionProvider && editorTextFocus && !inReferenceSearchEditor && !isInEmbeddedEditor` |
| <kbd>Alt</kbd> + <kbd>←</kbd> | `workbench.action.navigateBack` | Powrót do poprzedniego miejsca w historii nawigacji | — |
| <kbd>Alt</kbd> + <kbd>→</kbd> | `workbench.action.navigateForward` | Przejście do następnego miejsca w historii nawigacji | — |

### 🛠️ Refaktoryzacja i edycja kodu

| Skrót | Polecenie | Działanie | Warunek (`when`) |
| :--- | :--- | :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd> | `editor.action.refactor` | Wywołuje menu refaktoryzacji (np. wyodrębnienie metody/zmiennej) | `editorHasCodeActionsProvider && editorTextFocus && !editorReadonly` |
| <kbd>F2</kbd> | `editor.action.rename` | Zmienia nazwę zmiennej lub metody w całym projekcie | `editorHasRenameProvider && editorTextFocus && !editorReadonly` |
| <kbd>Ctrl</kbd> + <kbd>/</kbd> | `editor.action.commentLine` | Komentuje lub odkomentowuje zaznaczony blok tekstu | `editorTextFocus && !editorReadonly` |
| <kbd>Ctrl</kbd> + <kbd>D</kbd> | `editor.action.addSelectionToNextFindMatch` | Zaznacza kolejne identyczne wystąpienie dla multikursora | `editorFocus` |
| <kbd>Alt</kbd> + <kbd>↑</kbd> | `editor.action.moveLinesUpAction` | Przesuwa bieżącą linię lub zaznaczenie w górę | `editorTextFocus && !editorReadonly` |
| <kbd>Alt</kbd> + <kbd>↓</kbd> | `editor.action.moveLinesDownAction` | Przesuwa bieżącą linię lub zaznaczenie w dół | `editorTextFocus && !editorReadonly` |
| <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>↓</kbd> | `editor.action.copyLinesDownAction` | Duplikuje bieżącą linię w dół | `editorTextFocus && !editorReadonly` |

### 🪟 Zarządzanie oknami i widokiem

| Skrót | Polecenie | Działanie | Warunek (`when`) |
| :--- | :--- | :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>B</kbd> | `workbench.action.toggleSidebarVisibility` | Pokazuje lub ukrywa boczny pasek z drzewem plików | — |

---

## 🚀 Jak użyć w swoim VS Code

1. W Visual Studio Code naciśnij <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>.
2. Wpisz i wybierz: **`Preferences: Open Keyboard Shortcuts (JSON)`**.
3. Skopiuj zawartość pliku [`keybindings.json`](./keybindings.json) i wklej do otwartego pliku w edytorze.
4. Zapisz plik (<kbd>Ctrl</kbd> + <kbd>S</kbd>).
