# Konfiguracja repozytorium do pracy z Nozbe

> **Tłumaczenie — nie edytuj tego pliku bezpośrednio.**
> Wersją źródłową jest `setup.md` (angielski). Wprowadź zmiany tam, a następnie wygeneruj ten plik ponownie.

Użyj tego promptu w repozytorium, gdy Nozbe jest już połączone przez MCP. Sprawdza Nozbe, pyta mnie o to, czego brakuje, i zapisuje wynik w CLAUDE.md repozytorium, żeby `nozbe.md` wiedziało, z jakiego zespołu, osób i projektu korzystać.

## Kroki

1. **Sprawdzasz połączenie.** Potwierdzasz, że masz dostęp do Nozbe, i sprawdzasz, które konto jest zalogowane. Jeśli nie masz dostępu, przerywasz i mówisz mi, żebym najpierw połączył Nozbe przez MCP.
2. **Agent.** Połączenie MCP musi korzystać z konta agenta, a nie dyrektora. Pokazujesz mi zalogowane konto i pytasz, czy to agent. Jeśli nie, mówisz mi, żebym wylogował się z aplikacji desktopowej Nozbe, zalogował jako agent i odświeżył połączenie MCP, a potem sprawdzasz ponownie. Gdy potwierdzę, że zalogowany jest agent, bierzesz nazwę użytkownika i identyfikator agenta z tego konta.
3. **Zespół.** Wypisujesz zespoły (przestrzenie), do których należy agent, i pytasz, w którym z nich pracuje to repozytorium. Jeśli jest tylko jeden, prosisz mnie o potwierdzenie.
4. **Dyrektor.** Wypisujesz pozostałych członków tego zespołu i pytasz, który z nich to ja, dyrektor.

   Dla obu osób zapisujesz nazwę użytkownika w Nozbe (tę, którą pisze się po „@” we wzmiance) i identyfikator w tym zespole. Jeśli nazwa użytkownika nie jest widoczna, pytasz mnie o nią.
5. **Projekt.** Ustalasz nazwę repozytorium (nazwę jego folderu). Szukasz w zespole projektu o tej samej nazwie.
   - Jeśli taki jest, prosisz mnie o potwierdzenie, że to projekt tego repozytorium.
   - Jeśli go nie ma, proponujesz jego utworzenie. Gdy się zgodzę, tworzysz w zespole projekt o nazwie repozytorium, widoczny dla całego zespołu.
6. **Zapisujesz CLAUDE.md.** Pokazujesz mi, co dodasz, a gdy się zgodzę, dodajesz to do CLAUDE.md repozytorium (tworzysz plik, jeśli nie istnieje):

   ```markdown
   ## Nozbe

   - Zespół: [nazwa zespołu] (ID: [team_id])
   - Dyrektor: @[nazwa_użytkownika] (ID: [user_id])
   - Agent: @[nazwa_użytkownika] (ID: [user_id])
   - Projekt: [nazwa projektu] (https://nozbe.app/teams/[team_id]/projects/[project_id])
   ```
7. **Zasady.** Gdy konfiguracja Nozbe jest gotowa, pytasz mnie, jak dodać zasady, czyli `nozbe.pl.md` z https://github.com/Nozbe/AgentRules:
   - **Skopiować je.** Pobierasz `nozbe.pl.md` z repozytorium i wklejasz jego zawartość do CLAUDE.md.
   - **Dodać odwołanie.** Dodajesz `@nozbe.pl.md` do CLAUDE.md. Sam skopiuję `nozbe.pl.md` do repozytorium.
8. **Potwierdzasz.** Mówisz mi, co zostało skonfigurowane.
