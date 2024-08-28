# zacznij programowanie

## Podstawy

1. wejście-przetwarzanie-wyjście.
2. każdy program da się napisać instrukcją `if` oraz `while`.
3. dane przechowujemy w zmiennej. tablica to ułatwienie dla programisty. to grupa zmiennych do których można się dostać po numerze.
4. funkcje to ułatwienie dla programisty. grupują powtarzalny kod jak szablon.

## Nauka

1. ucz się na początek jednego języka programowania, aż go dobrze poznasz.
2. aby dobrze poznać język programowania, trzeba napisać w nim duży projekt np. 100k linii kodu.
3. najlepiej się uczyć robiąc projekty np. https://www.udemy.com/course/nauka-pythona-poprzez-tworzenie-gier-w-pygame-zero/
4. gromadź swoją wiedzę gdzieś: https://obsidian.md - można synchronizować do swojego repozytorium git, https://docusaurus.io/
5. https://roadmap.sh/

## Edytory kodu

1. cursor.sh
2. vscode
3. neovim
4. zed

## Przydatne

1. bash
2. git
3. sql

## Przydatne - następny poziom

1. wyrażenia regularne
2. system binarny, szestnastkowy itp.


## idee

1. złożoność to podstawowy wróg programisty: https://grugbrain.dev, KISS, YAGNI.
2. https://danielchasehooper.com/posts/good-ideas-in-cs/

## Paradygmaty itp.

1. imperatywny
2. funkcyjny - może być trudne do czytania i zarządzania jak dużo lambd.

<details><summary>Andrew Kelley jest przeciwny</summary>Finally, I personally despise the functional programming style that uses lambdas everywhere. I find it very difficult to read and maintain code that makes heavy use of inversion of control flow. By not accepting this proposal, Zig will continue to encourage programmers to stick to an imperative programming style, using for loops and iterators. https://github.com/ziglang/zig/issues/1717#issuecomment-1627790251</details>
   
5. zorientowany obiektowo
6. język dynamiczny vs typowany
7. TDD bad

<details><summary>więcej</summary>
I work for a Danish municipality and we buy quite a lot of development from various software houses. Being the public sector we track and benchmark almost everything, and we actually have a dataset on automated testing that’s been running for two decades.
It’s hard to use the data, because we’re comparing different projects, teams and suppliers but our data shows no advantage in choosing the companies that are very test-focused.
They are often slower, more expensive but have the same amount of incident reports as the companies which tests less or doesn’t do automated test at all.
   
https://news.ycombinator.com/item?id=20976397
   

I'd take a slightly different take:
- Structure your code so it is mostly leaves.
- Unit test the leaves.
- Integration test the rest if needed.
I like this approach in part because making lots of leaves also adds to the "literate"-ness of the code. With lots of opportunities to name your primitives, the code is much closer to being self documenting.
Depending on the project and its requirements, I also think "lazy" testing has value. Any time you are looking at a block of code, suspicious that it's the source of a bug, write a test for it. If you're in an environment where bugs aren't costly, where attribution goes through few layers of code, and bugs are easily visible when they occur, this can save a lot of time.
My leaves are either pure functions (FP languages) or value objects that init themselves based on other value objects (OOP languages). These value objects have no methods, no computed properties, etc. Just inert data.
No mocks and no “header” interfaces needed.
On top of that I sprinkle a bunch of UI tests to verify it’s all properly wired up.

https://news.ycombinator.com/item?id=15565875

I'm grateful for what TDD did to open my eyes to automated regression testing, but I've long since moved on from the design dogma.
Test-first units leads to an overly complex web of intermediary objects and indirection in order to avoid doing anything that's "slow". Like hitting the database. Or file IO. Or going through the browser to test the whole system. It's given birth to some truly horrendous monstrosities of architecture. A dense jungle of service objects, command patterns, and worse.

https://dhh.dk/2014/tdd-is-dead-long-live-testing.html
</details>

6. Brian Fitzpatrick

<details><summary>jego sposób</summary>

Seibel: Jak projektujesz sworogramowanie?

Fitzpatrick: Zaczynam od interfejsów łączących poszczególne elementy. Identyfikuję typowe metody, typowe wywołania RPC lub typowe zapytania. Jeśli chodzi o składowanie danych, staram się określić najbardziej typowe zapytania. Oceniam, których indeksów będziemy potrzebować. Zastanawiam się nad strukturą danych przechowywanych na dysku. Później piszę uproszczone wersje poszczególnych elementów systemu i zaczynam je stopniowo rozwijać.

Seibel: Wykorzystujesz te próbki w roli testów (w myśl zasady: najpierw testy), aby w przyszłości testować rozwijane rozwiązania?

Fitzpatrick: Robię tak coraz częściej. Zawsze projektowałem oprogramowanie w ten sposób, nawet wtedy, gdy nie przywiązywałem wagi do testów. Zaczynałem od projektowania interfejsów i sposobu składowania danych, by następnie przystąpić do właściwej implementacji.

Seibel: Jaką formę przybiera taki projekt? Pseudokodu? Właściwego kodu? Bazgrołów na tablicy?

Fitzpatrick: Najczęściej po prostu otwieram edytor i sporządzam notatki dotyczące projektowanego schematu wraz z elementami pseudokodu. Kiedy projekt w tej formie osiąga stan, który mnie satysfakcjonuje, przygotowuję prawdziwy schemat oraz kopiuję i wklejam gotowe elementy kodu, aby mieć pewność, że przynajmniej wyrażenia create table działają jak należy. Kiedy już wszystko na tym etapie wydaje mi się dopięte na ostatni guzik, przystępuję do implementacji tak zapisanych koncepcji. Zawsze zaczynam od pliku spec.txt.

Seibel: Czy już po napisaniu kiedykolwiek odkryłeś, że musisz zrewidować swój oryginalny plan?

Fitzpatrick: Czasami. Zawsze jednak zaczynałem pracę od najtrudniejszych elementów lub od koncepcji, których nie byłem pewien — te elementy implementowałem w pierwszej kolejności. Staram się nie odkładać na ostatnią chwilę tego, co najtrudniejsze lub najbardziej zaskakujące; lubię zaczynać od najtrudniejszych aspektów. We wszystkich projektach, których nigdy nie skończyłem — moi znajomi zarzucają mi, że była ich cała masa — faktycznym powodem niepowodzeń było właśnie rozpoczynanie prac od najtrudniejszych elementów, odkrywanie, że muszę się czegoś nauczyć, i ostateczna rezygnacja z realizacji najbardziej nudnych aspektów.
</details>

## Debugowanie

1. zakomentuj część kodu jak w wyszukiwaniu binarnym
2. print debugging
3. breakpoints i step-by-step, step-inside

## Algorytmy, ćwiczenia 

1. https://exercism.org/
2. https://leetcode.com/studyplan/
3. https://x.com/NeetAcc/status/1828059231120961655
4. https://x.com/NeetAcc/status/1828111694616559719
