# Git Branches

> Branches (Zweige) erlauben es dir, unabhängig vom Hauptcode an neuen Features oder Fehlerbehebungen zu arbeiten, ohne die stabile Version zu gefährden.

## Branches verwalten und anzeigen

> Listet alle vorhandenen Branches auf und zeigt dir, auf welchem Branch du dich aktuell befindest.

1. Lokale Branches anzeigen:

```bash
git branch
```

2. Alle lokalen und entfernten (Remote) Branches anzeigen:

```bash
git branch -a
```

> Der aktuelle Branch wird in der Ausgabe mit einem Sternchen (`*`) markiert.

## Neuen Branch erstellen

> Erstellt eine exakte Kopie deines aktuellen Arbeitsstandes unter einem neuen Namen.

1. Einen neuen Branch erstellen:

```bash
git branch feature-neue-funktion
```

> Dieser Befehl erstellt den Branch nur. Du wechselst dadurch noch nicht automatisch dorthin.

## Branches wechseln

> Wechselt den Arbeitsbereich auf einen anderen bestehenden Branch.

1. Auf einen vorhandenen Branch wechseln:

```bash
git checkout feature-neue-funktion
```
*(Alternativ):*
```bash
git switch feature-neue-funktion
```

2. Einen neuen Branch erstellen und sofort dorthin wechseln:

```bash
git checkout -b feature-neue-funktion
```
*(Alternativ):*
```bash
git switch -c feature-neue-funktion
```

## Branches löschen

> Entfernt Branches, die nicht mehr benötigt werden (z. B. nach einem erfolgreichen Merge).

1. Einen Branch sicher löschen:

```bash
git branch -d feature-neue-funktion
```

2. Das Löschen eines Branches erzwingen:

```bash
git branch -D feature-neue-funktion
```
