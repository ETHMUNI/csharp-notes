# C SHARP

## Intro

### Tasks
* Task bruges til asynkronks opgaver. Her bruges der await og async.
* Tasks minder lidt om Futures i java.
* Tasks kan også godt være Generic: ```Task<T> = Task<int>``` Her lover den at returnere en int i fremtiden.

## Unikke funktioner i C# (som ikke findes i Java)

1. Pattern Matching:
* Giver en mere kortfattet og fleksibel syntaks til komplekse beslutningslogikker via is og pattern-baserede switch.

2. String interpolation og raw string literals:
* Brug ${expression} til at indsætte udtryk i strenge.
* Raw string literals gør det nemmere at håndtere tekst med mange escape-tegn.

3. Nullable og ikke-nullbare typer:
* Ved at tilføje ? til en datatype, kan du angive, at den kan være null.
* Kompilatoren hjælper med at undgå NullReferenceException ved at kræve null-checks.

4. Extension Methods:
* Mulighed for at udvide eksisterende klasser eller interfaces uden at ændre deres kode.

5. LINQ (Language Integrated Query):
* En ensartet syntaks til forespørgsler og transformation af data, uanset om det er fra lister, databaser eller filer.

6. Lokale funktioner:
* Mulighed for at definere funktioner inden i metoder for at kapsle dem yderligere.

7. Records:
* Bruges til at definere dataobjekter. Kan være enten reference- eller værdityper og understøtter immutability.

8. Asynkron programmering med async og await:
* Enkle og effektive værktøjer til at håndtere asynkronitet uden at skulle bruge tråde manuelt.

9. Indexers:
* Tillader, at klasser kan behandles som arrays eller ordbøger med brugerdefineret syntaks.
