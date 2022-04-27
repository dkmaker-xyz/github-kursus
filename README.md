# Hvad skal vi idag?

- Hvad er Git?
  - Eller Github?
  - Source Control kort fortalt
- Git begreber
  - Repository
  - Branch
  - Add
  - Commit
  - Pull / Push
  - Pull Request
  - Master / Main
- Hvordan kan man bruge Git?
  - [cli](#cli)
  - Sæt Username / Email
  - Visual Studio Code (VSCode) X
  - GitHub Desktop X
  - Og mange mange flere...
- Anvendelsesområder
  - Source control
    - Både alene X
    - Og i Teams X
- Praktiske eksempler
  - Oprette et Git Repository
    - Nyt Repository
    - Allerede eksisterende kode
  - VSCode Integration
    - Hvorfor elsker jeg dette?
  - GitHub Pages
    - HTML/Markdown uden en server via *.github.io eller eget domain!
  - Nyttige kommandoer
    - git status
- Branching Strategier
  - [Trunk Based](#trunk-based)

# Hvad er Git?

Git bliver brugt mellem flere medlemmer af et team - eller kan bruges alene bare for at holde styr på sin kode.

![Git Eksempel](img/distributed-vcs.png)

## Git eller Github?

Github er ikke Git, GitHub er en service til at lægge din kode op i Git formatet, GitHub facilitere blot sikkerhed, dokumentation, projektstyring etc. rundt om Git formatet. Der findes mange alternativer til GitHub - men Github er den mest brugte.

Af alternativer kan nævnes GitLab, Azure DevOps, Bitbucket, GitBucket etc.

# Git begreber

Der er mange ord / ting i Git som godt kan give en ret stejl indlæringskurve herunder render vi kort indt i dem

## Repository

En mappe der er "tracked" med Git, dvs. der er formentlig en .git mappe i roden af denne mappe.

.git mappen indeholder alle versioner etc. af filer i repository dvs. ud fra den database der ligger i .git mappen kan man gå point in time tilbage til alle ændringer samt se sin log via git.exe eller f.eks. VSCode

## Branch

En gren af koden - standard branch hedder enten master eller main - [anekdote tid](https://faktalink.dk/titelliste/slaveriet-i-usa/slaveriets-efterspil)

Opret ny fra aktuel
```
git.exe branch test-branch
```

## Add

Før en fil kan committes skal man vælge at tilføje den til sin Stage area (Filer der er ændret som skal med i commit)

Opret ny fra aktuel
```
git.exe add main.cpp
git add .
```

## Commit

Du gemmer et "snapshot" af din kode med en besked i den pågældende branch du er i - en commit er en lokal ting - denne er først gemt online når den er "Pushed" online

Commit aktuel kode
```
git.exe branch test-branch
```

## Pull/Push

Pull / Push gør det det siger - man henter eller sender rettelser til det kode man har

## Pull Request
## Master / Main

# Source Control kort fortalt

Source Control bruges til at organisere tekstfiler og tekst indhold på en måde hvor du kan spore ændringer, merge / diff filer for at se hvad er ændret.

Ud over dette får man også en organiseret "backup" af din kildekode, og man åbner op for man kan lave midlertidige ændringer i kildekoden og bare smide det væk igen uden at man skal holde styr på ens filer heletiden med mange kopier.

Jeg plejer at sige at mit Git er det eneste sted sandheden er - alt andet er usikre filer!

## Hvoran kan man bruge Git?

Der er mange måder at bruge Git på.

### cli

Til at snakke med git via cli har man **git.exe** som man kan installere fra [https://git-scm.com/](https://git-scm.com/)

```
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone             Clone a repository into a new directory
   init              Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add               Add file contents to the index
   mv                Move or rename a file, a directory, or a symlink
   restore           Restore working tree files
   rm                Remove files from the working tree and from the index
   sparse-checkout   Initialize and modify the sparse-checkout

examine the history and state (see also: git help revisions)
   bisect            Use binary search to find the commit that introduced a bug
   diff              Show changes between commits, commit and working tree, etc
   grep              Print lines matching a pattern
   log               Show commit logs
   show              Show various types of objects
   status            Show the working tree status

grow, mark and tweak your common history
   branch            List, create, or delete branches
   commit            Record changes to the repository
   merge             Join two or more development histories together
   rebase            Reapply commits on top of another base tip
   reset             Reset current HEAD to the specified state
   switch            Switch branches
   tag               Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch             Download objects and refs from another repository
   pull              Fetch from and integrate with another repository or a local branch
   push              Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
```

### Sæt Username / Email

Alle commits etc. bliver påført hvem der har lavet det så før man kan committe / bruge git skal git vide hvem man er og det kan sættes via nedenstående kommando.

```
git config --global user.name "Dit fulde navn"
git config --global user.email "Den email adresse du logger på GitHub med"
```

## Branching Strategier

### Trunk Based

Det kan også være rigtig enkelt med Trunk Based

![TrunkBased](img/trunk-based-development-branching-strategy.png)

### Git Flow

Det kan være meget kompliceret med GitFlow strategien

![Kompliceret](img/gitflow-branching-strategy.png)
