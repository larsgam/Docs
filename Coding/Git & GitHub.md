# Git & GitHub – Hurtigt Overblik

## 1. Start et nyt projekt

git init

## 2. Tjek status

git status

## 3. Tilføj ændringer til staging

Tilføj en bestemt fil:
git add filnavn.py

Tilføj alt:
git add .

## 4. Commit dine ændringer

git commit -m "Beskrivelse af ændringer"

## 5. Opret forbindelse til GitHub

git remote add origin git@github.com:larsgam/Docs.git

## 6. Push første gang (ny branch)

git push -u origin main

Al efterfølgende push:
git push

## 7. Hent ændringer fra GitHub

git pull

## 8. Branching

Opret en branch:
git branch feature-navn

Skift til branch:
git switch feature-navn

Opret + skift:
git switch -c feature-navn

Se branches:
git branch

## 9. Merge en branch ind i main

git switch main
git merge feature-navn

## 10. Se commit-historik

Kort historik:
git log --oneline

Fuld historik:
git log

## 11. Undo og reset (mest brugt)

Fjern fil fra staging:
git restore --staged filnavn.py

Tilbagefør ændringer i fil:
git restore filnavn.py

## 12. Klon et GitHub-repo

git clone https://github.com/brugernavn/repo.git

## 13. Sæt main som default branch (hvis projekt starter med master)

git branch -M main

## 14. Se forskelle

git diff

---

# Hurtigt workflow for daglig brug

## Første gang i et nyt projekt:

git init
git add .
git commit -m "First commit"
git branch -M main
git remote add origin https://github.com/brugernavn/repo.git
git push -u origin main

## Efterfølgende:

git add .
git commit -m "Fixet X, tilføjet Y"
git push
