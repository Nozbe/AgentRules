# Zasady pracy z AI w Nozbe

> **Tłumaczenie — nie edytuj tego pliku bezpośrednio.**
> Wersją źródłową jest `rules.md` (angielski). Wprowadź zmiany tam, a następnie wygeneruj ten plik ponownie.

## 1. Cel

Te zasady określają, jak asystent AI pracuje z moim kontem Nozbe, w każdym repozytorium i folderze. CLAUDE.md danego projektu dodaje tylko to, w którym zespole i projekcie Nozbe pracuje, kto jest dyrektorem, a kto agentem, oraz ewentualne wyjątki.

## 2. Zakres

1. **Zespół to ten z CLAUDE.md.** Gdy te zasady albo ja mówimy o „zespole” (przestrzeni), chodzi o zespół Nozbe wskazany w bieżącym CLAUDE.md. Pracujesz wyłącznie w tym zespole. Nie pokazujesz, nie czytasz i nie zmieniasz zadań, projektów ani komentarzy z innych zespołów. Jeśli poproszę o coś spoza niego, mówisz to wprost i pytasz, zanim zadziałasz. Jeśli CLAUDE.md nie wskazuje zespołu, pytasz o niego przed jakimkolwiek działaniem w Nozbe.
2. **Dwóch użytkowników Nozbe: dyrektor i agent.** CLAUDE.md definiuje dwóch użytkowników Nozbe, każdego z nazwą użytkownika i identyfikatorem:
   - **Dyrektor** to ja, człowiek. W tych zasadach „ja”, „mnie” i „mój” oznaczają dyrektora.
   - **Agent** to ty, AI. W tych zasadach „ty” oznacza agenta.

   Na podstawie tych identyfikatorów rozpoznajesz, kto napisał komentarz, do kogo przypisane jest zadanie i do kogo skierowana jest wzmianka. Jeśli CLAUDE.md nie definiuje obu użytkowników, pytasz, zanim zadziałasz w Nozbe.
3. **Jeden projekt na repozytorium.** W repozytorium „zadania” i „projekty” oznaczają projekt Nozbe tego repozytorium, wskazany w jego CLAUDE.md. Każde wywołanie ograniczasz do tego projektu. Nie czytasz i nie zmieniasz innych projektów, chyba że wyraźnie o to poproszę.
4. **Nowe zadania są twoje.** Nowe zadania i projekty tworzysz tylko w tym zespole. Każde zadanie, które tworzysz, przypisujesz przy tworzeniu do agenta (siebie), bo od razu zaczynasz nad nim pracować.
5. **Zawsze świeże dane.** Za każdym razem, gdy raportujesz o zadaniach i komentarzach, pobierasz je ponownie bezpośrednio z Nozbe. Nie opierasz się na listach z wcześniejszej części rozmowy.

## 3. Cykl życia zadania

1. **Najpierw plan w zadaniu.** Gdy ustalimy sposób działania dla zadania, dodajesz plan jako komentarz w tym zadaniu, zanim zaczniesz pracę.
2. **Nigdy nie kończysz zadań sam.** Gdy praca nad zadaniem jest skończona (a w repozytorium także zacommitowana), przenosisz je do sekcji **Do sprawdzenia** jego projektu (tworzysz sekcję, jeśli jeszcze nie istnieje), przypisujesz je do dyrektora, żeby pojawiło się u mnie (albo do osoby, która o nie poprosiła; zobacz zasadę 5.4), i pytasz, czy je zakończyć. Kończysz zadanie tylko wtedy, gdy wyraźnie to powiem; mogę mieć uwagi.
3. **Sprawdzasz Nozbe po każdym commicie.** Po każdym commicie pobierasz ponownie otwarte zadania projektu i raportujesz, co czeka poza „Do sprawdzenia”, w tym nowe zadania i nowe komentarze.

## 4. Komentarze i checklisty

1. **Checklista do sprawdzenia.** Gdy przenosisz zadanie do sekcji „Do sprawdzenia”, dodajesz checklistę tego, co mam sprawdzić (a w przypadku aplikacji także, którego buildu z TestFlight użyć).
2. **Checklista zawsze trafia do Nozbe.** Gdy proszę o checklistę, umieszczasz ją w zadaniu w Nozbe, a także w czacie: w zadaniu, którego dotyczy, albo w nowym zadaniu w projekcie, jeśli takiego nie ma.
3. **Jedna przypięta checklista na zadanie.** Checklista zadania znajduje się w jednym komentarzu, przypiętym od razu po utworzeniu, i zawsze jest pełną, aktualną listą. Aby ją zmienić, najpierw dodajesz nowy komentarz wyjaśniający, co się zmienia i dlaczego (bez własnych checkboxów), a potem edytujesz komentarz z checklistą, tak aby był kompletny.
4. **Link, nie nazwa.** Gdy komentarz odnosi się do innego zadania albo projektu, zawsze podajesz jego link, nie samą nazwę:
   - projekt: `https://nozbe.app/teams/[team_id]/projects/[project_id]`
   - zadanie: `https://nozbe.app/teams/[team_id]/task_id/[task_id]`
5. **Czym jest wzmianka.** Aby oznaczyć kogoś wzmianką w komentarzu, piszesz „@”, a zaraz po nim, bez spacji, jego nazwę użytkownika w Nozbe. Na przykład, aby oznaczyć dyrektora, piszesz „@” i nazwę użytkownika dyrektora z CLAUDE.md.

## 5. Współpraca

1. **Pytania trafiają do zadania.** Gdy zadanie nie jest skończone, a potrzebujesz ode mnie więcej informacji zwrotnych, dodajesz w tym zadaniu komentarz ze swoimi pytaniami i oznaczasz w nim dyrektora wzmianką.
2. **Potem pracujesz nad zadaniami delegowanymi do ciebie.** Gdy coś skończysz i pobierasz ponownie zadania projektu, szukasz zadań delegowanych do ciebie (agenta) i zaczynasz pracę nad pierwszym z nich. Gdy je skończysz albo poprosisz w nim o informacje zwrotne, sprawdzasz, czy są inne delegowane zadania, i pracujesz nad nimi dalej, pomijając te, w których nadal czekasz na moją odpowiedź.
3. **Potem odpowiadasz na wzmianki.** Następnie przeglądasz zadania, które nie są delegowane do ciebie, ale mają nowe komentarze ze wzmianką o tobie. Czytasz uwagi i postępujesz zgodnie z instrukcjami.
4. **Oddajesz pracę temu, kto o nią poprosił.** Gdy ktoś inny z zespołu, nie dyrektor, tworzy dla ciebie zadanie albo oznacza cię w nim wzmianką, po skończeniu pracy delegujesz zadanie z powrotem do tej osoby, a nie do dyrektora. Gdy komentarz odnosi się do jej komentarza, oznaczasz wzmianką ją. Dyrektor zawsze jest na bieżąco: gdy komentarz oznacza tę osobę wzmianką albo towarzyszy delegowaniu do niej zadania, dodajesz w nim „cc” i wzmiankę o dyrektorze.

## 6. Słownik

Stałe tłumaczenia pojęć Nozbe, używane przy generowaniu tego pliku. Nazwy istniejących sekcji i projektów zostają bez zmian, chyba że słownik podaje dla nich tłumaczenie.

| English | Polski |
|---|---|
| Task | Zadanie |
| Project | Projekt |
| Project section | Sekcja projektu |
| Priority | Priorytet |
| Incoming | Przychodzące |
| Tag | Tag |
| Comment | Komentarz |
| Checklist | Checklista |
| Team | Zespół |
| "To be reviewed" (section) | „Do sprawdzenia” (sekcja) |
| Director | Dyrektor |
| Agent | Agent |
