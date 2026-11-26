# AgentRules

English version: [README.md](README.md)

Zestaw zasad pracy z agentami AI w Nozbe przez lokalne połączenie MCP.

[Nozbe](https://nozbe.com) to aplikacja do zarządzania zadaniami i projektami dla zespołów. Agenci AI mogą dołączyć do zespołu w Nozbe, pracować nad zadaniami i rozmawiać z ludźmi w komentarzach. Więcej o agentach AI w Nozbe przeczytasz na [nozbe.com/ai](https://nozbe.com/ai).

## Pliki

- [`nozbe.pl.md`](nozbe.pl.md): zasady pracy agenta AI w Nozbe — w którym zespole i projekcie pracuje, jak obsługuje zadania i komentarze oraz jak współpracuje z ludźmi.
- [`setup.pl.md`](setup.pl.md): prompt do wstępnej konfiguracji repozytorium. Sprawdza połączenie z Nozbe, pyta o zespół, dyrektora, agenta i projekt, a potem dodaje je wraz z zasadami do CLAUDE.md repozytorium. Może też ustawić sprawdzanie co 15 minut, dzięki któremu agent sam bierze się za delegowane do niego zadania.

Oba pliki są automatycznie tłumaczone z angielskich wersji źródłowych: [`nozbe.md`](nozbe.md) i [`setup.md`](setup.md).

## Jak pracować z członkiem zespołu w Nozbe, który jest… agentem AI?

1. [Załóż darmowe konto w Nozbe (albo Premium — śmiało!)](https://nozbe.com/). Nozbe jest darmowe bez limitu czasu dla maksymalnie 3 projektów i 3 osób w zespole (łącznie z agentami!), z nieograniczoną liczbą zadań, więc na start nie musisz nic płacić.
2. Gdy masz już konto, zaproś agenta AI do swojego zespołu. Wejdź w „Członkowie przestrzeni”, kliknij „+” („Dodaj nową osobę”) i podaj inny adres e-mail, do którego masz dostęp, żeby potwierdzić i założyć konto agenta. Otwórz konto agenta w innej sesji przeglądarki i je skonfiguruj. Nadaj agentowi imię i opcjonalnie awatar (czemu nie?). Możesz użyć [`agent.png`](agent.png) z tego repozytorium.
3. Pobierz [aplikację desktopową Nozbe](https://nozbe.com/download) na Windowsa lub Maca i zainstaluj ją.
4. Zaloguj się w aplikacji desktopowej na konto agenta. Nie na swoje. Na konto agenta!
5. Wejdź w „Ustawienia” → „Integracje” → „MCP” i włącz lokalne połączenie MCP.
6. Skopiuj polecenie `claude mcp add …`, które pokazuje tam Nozbe. Potem otwórz Claude Code w folderze (nowym lub istniejącym), w którym chcesz pracować z agentem, i wklej polecenie do czatu. Claude je uruchomi i doda połączenie z Nozbe. Następnie zacznij nowy czat, żeby Claude je wczytał.
7. W tym nowym czacie wklej prompt z [`setup.pl.md`](setup.pl.md), żeby skonfigurować agenta.
8. Od teraz możesz pracować z agentem bezpośrednio w Nozbe: delegować mu zadania i rozmawiać w komentarzach. Powodzenia!

Masz pytania? Napisz do mnie, autora tego repozytorium: [Michał Śliwiński, CEO Nozbe](https://michael.team/pl/).

## Ulepszenia?

Pomysły na ulepszenie konfiguracji? Lepsze zasady współpracy? Pull requesty mile widziane!
