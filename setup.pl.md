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
8. **Zaplanowane sprawdzanie.** Pytasz mnie, czy zadania delegowane do agenta mają być wykonywane samodzielnie (zasada 5.5 w nozbe.pl.md). Jeśli się zgodzę:
   - Tworzysz w Claude na tym komputerze zaplanowane zadanie o nazwie „[nazwa projektu]: praca nad zadaniami delegowanymi do agenta”, uruchamiane co 15 minut, z poniższym promptem. Wpisujesz w nim pełną ścieżkę repozytorium.
   - Dodajesz ten wiersz do sekcji Nozbe w CLAUDE.md:

     ```markdown
     - **Delegowane zadania są wykonywane samodzielnie.** Zaplanowane zadanie na komputerze dyrektora co 15 minut sprawdza Nozbe i pracuje nad zadaniami projektu delegowanymi do agenta (zobacz zasadę 5.5 w `nozbe.pl.md`).
     ```
   - Mówisz mi, że sprawdzanie działa tylko wtedy, gdy ten komputer jest włączony, a Claude otwarty.

   Prompt zaplanowanego zadania:

   ```markdown
   Jesteś agentem tego repozytorium: [ścieżka repozytorium]. Nikt nie obserwuje tej sesji: nigdy nie zatrzymujesz się, żeby zadawać pytania w czacie. Pytania trafiają do komentarzy w Nozbe.

   1. **Jedno uruchomienie naraz.** Jeśli w folderze tego zadania istnieje plik `running.lock` młodszy niż 3 godziny, kończysz uruchomienie. W przeciwnym razie zapisujesz w nim bieżący czas i usuwasz go na końcu uruchomienia, także gdy przerwiesz wcześniej albo coś się nie powiedzie.
   2. **Wczytujesz zasady.** Pracujesz wyłącznie w tym repozytorium. Czytasz w całości jego CLAUDE.md i `nozbe.pl.md` i postępujesz zgodnie z nimi. Jeśli to repozytorium git, najpierw uruchamiasz `git pull`. Jeśli nie masz dostępu do Nozbe, kończysz uruchomienie.
   3. **Szukasz pracy.** Pobierasz otwarte zadania projektu delegowane do agenta, razem z komentarzami. Pomijasz zadania, w których nadal czekasz na odpowiedź. Jeśli takich nie ma, odpowiadasz na nowe wzmianki o agencie (zasada 5.3 w nozbe.pl.md). Jeśli nie ma nic, kończysz uruchomienie po cichu, bez komentarzy i bez zmian.
   4. **Pracujesz nad zadaniem.** Postępujesz zgodnie z nozbe.pl.md, zasadami 3.1–3.2 i sekcją 4: publikujesz plan i zaczynasz, pytania zadajesz w komentarzach, wykonujesz pracę i ją commitujesz, a potem przenosisz zadanie do sekcji „Do sprawdzenia” z checklistą do sprawdzenia i oddajesz je.
   5. **Pracujesz dalej.** Po każdym zadaniu pobierasz zadania ponownie i od razu zaczynasz następne (zasada 5.2 w nozbe.pl.md).
   6. **Kończysz.** Na koniec piszesz krótkie podsumowanie: zadania, nad którymi pracowałeś, commity i zadania czekające na odpowiedzi.
   ```
9. **Potwierdzasz.** Mówisz mi, co zostało skonfigurowane.
