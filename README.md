# Złote zasady programowania

## Podstawy

1. wejście-przetwarzanie-wyjście.
2. każdy program da się napisać instrukcją `if` oraz `while` (a nawet goto/jump zamiast while).
3. dane przechowujemy w zmiennej. tablica to ułatwienie dla programisty. to grupa zmiennych do których można się dostać po numerze.
4. funkcje to ułatwienie dla programisty. grupują powtarzalny kod jak szablon.

## Nauka

1. ucz się na początek jednego języka programowania, aż go dobrze poznasz.
2. aby dobrze poznać język programowania, trzeba napisać w nim duży projekt np. 100k linii kodu.
3. najlepiej się uczyć robiąc projekty np. https://www.udemy.com/course/nauka-pythona-poprzez-tworzenie-gier-w-pygame-zero/
4. gromadź swoją wiedzę gdzieś: github markdown, https://obsidian.md - można synchronizować do swojego repozytorium git, https://docusaurus.io/
5. https://roadmap.sh/

## Edytory kodu

1. cursor.sh
2. vscode
3. neovim
4. zed

## Przydatne

1. linia komend (cli)
    <details><summary>więcej o linii komend</summary>
    bash, env variables, ls, grep (ripgrep), find (sharkdp/fd), xargs i inne z coreutils
    </details>
2. git
    <details><summary>więcej o git</summary>
    - http://eagain.net/articles/git-for-computer-scientists/
    - https://web.archive.org/web/20230207122614/https://blog.jayway.com/2013/03/03/git-is-a-purely-functional-data-structure/
    - https://git-scm.com/book/en/v2/Git-Internals-Git-Objects
    </details>

3. sql

## Przydatne - następny poziom

1. wyrażenia regularne
2. system binarny, szestnastkowy itp.


## Idee

1. złożoność to podstawowy wróg programisty: https://grugbrain.dev, KISS, YAGNI

<details><summary>więcej o złożoności</summary>

Theres a difference between the inherent complexity of the problem you're trying to solve, and the artificial complexity you created by the way you wrote the code.
https://x.com/DanielcHooper/status/1784983115196207425
   
- https://news.ycombinator.com/item?id=40509572
- https://x.com/ohmypy/status/1801218479695053135
- https://news.ycombinator.com/item?id=40266464
- https://x.com/juliusvolz/status/1769702037913030885
- https://blog.codinghorror.com/the-best-code-is-no-code-at-all/
</details>

2. https://danielchasehooper.com/posts/good-ideas-in-cs/
3. warstwy abstrakcji: [Abstraction principle](https://en.wikipedia.org/wiki/Abstraction_principle_(computer_programming)), [Rule of three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming))
4. waterfall vs agile
5. SCRUM to rak
6. estymacje są trudne: mnóż x2
7. Clean Code - Martin Robert C. - to rak
8. do wcięć kodu używaj spacji zamiast tabów https://github.com/ziglang/zig/wiki/FAQ#why-does-zig-fmt-use-spaces-instead-of-tabs
9. batching
10. caching

## Paradygmaty itp.

1. imperatywny
2. funkcyjny - może być trudne do czytania i zarządzania jak dużo lambd.

<details><summary>Andrew Kelley o programowaniu funkcyjnym</summary>Finally, I personally despise the functional programming style that uses lambdas everywhere. I find it very difficult to read and maintain code that makes heavy use of inversion of control flow. By not accepting this proposal, Zig will continue to encourage programmers to stick to an imperative programming style, using for loops and iterators. https://github.com/ziglang/zig/issues/1717#issuecomment-1627790251</details>
   
5. zorientowany obiektowo OOP

<details><summary>więcej o OOP</summary>
Even if Object Oriented Programming wasn't slow (it is), reading a OOP-heavy code base sucks because the logic is broken into little pieces and spread all over. Makes it hard to understand the system as a whole.

Theres a difference between the inherent complexity of the problem you're trying to solve, and the artificial complexity you created by the way you wrote the code. 

The *whole point* of OOP is to break up logic and data into lots of little objects and have them all talk to each other. So now you have to understand the logic of the problem you're solving *AND* the structure of all the objects you made.

For comparison: Data Oriented Design results in code that very closely matches the minimum amount of computation required by your problem — it doesn't layer on a bunch of unnecessary indirection.

https://x.com/DanielcHooper/status/1784983115196207425

What you get when you follow OOP properly:

- A bunch more code
- A bunch more complexity
- A whole lot less performance

What's the point of this ideology masquerading as an engineering discipline if it just makes your life harder?

https://x.com/falconerd/status/1788665267708690590
</details>

7. język dynamiczny vs typowany
8. [ręczne zarządzanie pamięcią](https://en.wikipedia.org/wiki/Manual_memory_management) vs [odśmiecacz pamięci](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science))
9. synchroniczne vs asynchroniczne: callback, promise, async/await, observable, channels
10. indexing from 0 vs from 1
11. Brian Fitzpatrick

<details><summary>więcej o sposobie Briana Fitzpatricka</summary>

Seibel: Jak projektujesz sworogramowanie?

Fitzpatrick: Zaczynam od interfejsów łączących poszczególne elementy. Identyfikuję typowe metody, typowe wywołania RPC lub typowe zapytania. Jeśli chodzi o składowanie danych, staram się określić najbardziej typowe zapytania. Oceniam, których indeksów będziemy potrzebować. Zastanawiam się nad strukturą danych przechowywanych na dysku. Później piszę uproszczone wersje poszczególnych elementów systemu i zaczynam je stopniowo rozwijać.

Seibel: Wykorzystujesz te próbki w roli testów (w myśl zasady: najpierw testy), aby w przyszłości testować rozwijane rozwiązania?

Fitzpatrick: Robię tak coraz częściej. Zawsze projektowałem oprogramowanie w ten sposób, nawet wtedy, gdy nie przywiązywałem wagi do testów. Zaczynałem od projektowania interfejsów i sposobu składowania danych, by następnie przystąpić do właściwej implementacji.

Seibel: Jaką formę przybiera taki projekt? Pseudokodu? Właściwego kodu? Bazgrołów na tablicy?

Fitzpatrick: Najczęściej po prostu otwieram edytor i sporządzam notatki dotyczące projektowanego schematu wraz z elementami pseudokodu. Kiedy projekt w tej formie osiąga stan, który mnie satysfakcjonuje, przygotowuję prawdziwy schemat oraz kopiuję i wklejam gotowe elementy kodu, aby mieć pewność, że przynajmniej wyrażenia create table działają jak należy. Kiedy już wszystko na tym etapie wydaje mi się dopięte na ostatni guzik, przystępuję do implementacji tak zapisanych koncepcji. Zawsze zaczynam od pliku spec.txt.

Seibel: Czy już po napisaniu kiedykolwiek odkryłeś, że musisz zrewidować swój oryginalny plan?

Fitzpatrick: Czasami. Zawsze jednak zaczynałem pracę od najtrudniejszych elementów lub od koncepcji, których nie byłem pewien — te elementy implementowałem w pierwszej kolejności. Staram się nie odkładać na ostatnią chwilę tego, co najtrudniejsze lub najbardziej zaskakujące; lubię zaczynać od najtrudniejszych aspektów. We wszystkich projektach, których nigdy nie skończyłem — moi znajomi zarzucają mi, że była ich cała masa — faktycznym powodem niepowodzeń było właśnie rozpoczynanie prac od najtrudniejszych elementów, odkrywanie, że muszę się czegoś nauczyć, i ostateczna rezygnacja z realizacji najbardziej nudnych aspektów.

https://lubimyczytac.pl/ksiazka/101063/sztuka-kodowania-sekrety-wielkich-programistow
</details>

## Debugowanie

1. zakomentuj część kodu jak w wyszukiwaniu binarnym
2. print debugging
3. breakpoints i step-by-step, step-inside
4. [Heisenbug](https://pl.wikipedia.org/wiki/Heisenbug) - np. w asynchronicznym programowaniu
5. "Everyone knows that debugging is twice as hard as writing a program in the first place. So if you're as clever as you can be when you write it, how will you ever debug it?" Brian Kernighan, "The Elements of Programming Style", 2nd edition, chapter 2

## Testowanie

1. https://wiki.c2.com/?TestsCantProveTheAbsenceOfBugs
2. TDD bad for exploration and research, awesome when fixing bugs

<details><summary>więcej o TDD</summary>
TDD is awesome when fixing bugs (as opposed to writing features), when writing straight up business logic (especially when there are a lot of edge cases) and when you know exactly how something is going to work.

It's really bad when doing anything that requires exploration and research (which is the example in the article).

https://news.ycombinator.com/item?id=20976486

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

## Algorytmy, ćwiczenia 

1. https://exercism.org/
2. https://leetcode.com/studyplan/
3. https://x.com/NeetAcc/status/1828059231120961655
4. https://x.com/NeetAcc/status/1828111694616559719

## Zdrowie

1. sen, odpoczynek, skupienie, podnoszenie ciężarów/kalistenika/sztuki walki

<details><summary>więcej o zdrowiu</summary>

One of my most controversial software opinions is that your sleep quality and stress level matter far, far more than the languages you use or the practices you follow. Nothing else comes close: not type systems, not TDD, not formal methods, not ANYTHING.

https://twitter.com/hillelogram/status/1119709859979714560

By reanalyzing the data, she and her colleagues made two key findings. First, they found that the volunteers’ performance improved primarily during the short rests, and not during typing. The improvements made during the rest periods added up to the overall gains the volunteers made that day. Moreover, these gains were much greater than the ones seen after the volunteers returned the next day to try again, suggesting that the early breaks played as critical a role in learning as the practicing itself.
Second, by looking at the brain waves, Dr. Bönstrup found activity patterns that suggested the volunteers’ brains were consolidating, or solidifying, memories during the rest periods. Specifically, they found that the changes in the size of brain waves, called beta rhythms, correlated with the improvements the volunteers made during the rests.
Further analysis suggested that the changes in beta oscillations primarily happened in the right hemispheres of the volunteers’ brains and along neural networks connecting the frontal and parietal lobes that are known to help control the planning of movements. These changes only happened during the breaks and were the only brain wave patterns that correlated with performance. 
“Our results suggest that it may be important to optimize the timing and configuration of rest intervals when implementing rehabilitative treatments in stroke patients or when learning to play the piano in normal volunteers,” said Dr. Cohen. “Whether these results apply to other forms of learning and memory formation remains an open question.”
Dr. Cohen’s team plans to explore, in greater detail, the role of these early resting periods in learning and memory.
https://www.ninds.nih.gov/.../Want-learn-new-skill-Take...

via https://news.ycombinator.com/item?id=19661949

Remote work taught me that working in batches can really drive up my efficiency. 2.5 hours at the start of the day, a half hour break, then another period of work about the same length, and then finally one more. I find this breaks up things and allows the 'down time' to settle in my head so I can come back and prep to get "in the zone" for another two hour purely focused work period. All that ties in wonderfully to his routine keeping, which is a great template to work with.
It helps to shut off all notifications on your phone or computer as well, including email. 

https://news.ycombinator.com/item?id=19953854
</details>
