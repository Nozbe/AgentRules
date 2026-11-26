# AgentRules

English version: [README.md](README.md)

Zestaw zasad pracy z agentami AI w Nozbe przez lokalne połączenie MCP.

[Nozbe](https://nozbe.com) to aplikacja do zarządzania zadaniami i projektami dla zespołów. Agenci AI mogą dołączyć do zespołu w Nozbe, pracować nad zadaniami i rozmawiać z ludźmi w komentarzach. Więcej o agentach AI w Nozbe przeczytasz na [nozbe.com/ai](https://nozbe.com/ai).

## Pliki

- [`nozbe.pl.md`](nozbe.pl.md): zasady pracy agenta AI w Nozbe — w którym zespole i projekcie pracuje, jak obsługuje zadania i komentarze oraz jak współpracuje z ludźmi.
- [`setup.pl.md`](setup.pl.md): prompt do wstępnej konfiguracji repozytorium. Sprawdza połączenie z Nozbe, pyta o zespół, dyrektora, agenta i projekt, a potem dodaje je wraz z zasadami do CLAUDE.md repozytorium. Może też ustawić sprawdzanie co 15 minut, dzięki któremu agent sam bierze się za delegowane do niego zadania.

Oba pliki są automatycznie tłumaczone z angielskich wersji źródłowych: [`nozbe.md`](nozbe.md) i [`setup.md`](setup.md).

## Jak pracować z kolegą z zespołu w Nozbe, który jest… agentem AI?

1. [Załóż darmowe konto w Nozbe (albo Premium — śmiało!)](https://nozbe.com/). Nozbe jest darmowe bez limitu czasu dla maksymalnie 3 projektów i 3 osób w zespole (wliczając agentów!), z nieograniczoną liczbą zadań, więc na start nie musisz nic płacić.
2. Gdy masz już konto, zaproś agenta AI do swojego zespołu. Wejdź w „Members”, kliknij „+”, żeby wybrać „Invite new member to your space”, i podaj inny adres e-mail, do którego masz dostęp, żeby potwierdzić i skonfigurować konto agenta. Otwórz konto agenta w innej sesji przeglądarki, żeby je skonfigurować. Nadaj mu nazwę i opcjonalnie awatar (czemu nie?). Możesz użyć [`agent.png`](agent.png) z tego repozytorium.
3. Pobierz [aplikację desktopową Nozbe](https://nozbe.com/download) na Windows lub Maca i zainstaluj ją.
4. Zaloguj się w aplikacji desktopowej na konto agenta. Nie swoje. Agenta!
5. Wejdź w „Settings” → „Integrations” → „MCP” i włącz lokalne połączenie MCP.
6. Skopiuj polecenie `claude mcp add …`, które pokazuje tam Nozbe. Potem otwórz Claude Code w folderze (nowym lub istniejącym), w którym chcesz pracować z agentem, i wklej polecenie do czatu. Claude je uruchomi i doda połączenie z Nozbe. Następnie zacznij nowy czat, żeby Claude je wczytał.
7. W tym nowym czacie wklej prompt z [`setup.pl.md`](setup.pl.md), żeby skonfigurować agenta.
8. Od teraz możesz pracować z agentem bezpośrednio w Nozbe: delegować mu zadania i rozmawiać w komentarzach. Powodzenia!

Masz pytania? Napisz do mnie, autora tego repozytorium: [Michael Sliwinski, CEO Nozbe](https://michael.team/).

## Ulepszenia?

Pomysły na ulepszenie konfiguracji? Lepsze zasady współpracy? Pull requesty mile widziane!
