# Git & GitHub – Hurtigt Overblik

## Hurtigt workflow for daglig brug

### Første gang i et nyt projekt:

* git init

* git add .

* git commit -m "First commit"

* git branch -M main

* git remote add origin https://github.com/brugernavn/repo.git 

* git push -u origin main

### Efterfølgende:

* git add .

* git commit -m "Fixet X, tilføjet Y"

* git push



## Flere commandoer

### 1. Start et nyt projekt

* `git init`

### 2. Tjek status

* `git status`

### 3. Tilføj ændringer til staging

* `git add filnavn.py` Tilføj en bestemt fil

* `git add .` Tilføj alt

### 4. Commit dine ændringer

* `git commit -m "Beskrivelse af ændringer"`

### 5. Opret forbindelse til GitHub

* `git remote add origin git@github.com:larsgam/repo.git`

### 6. Push første gang (ny branch)

* `git push -u origin main`

* `git push` Al efterfølgende push


### 7. Hent ændringer fra GitHub

* `git pull`

### 8. Branching

* `git branch feature-navn` Opret en branch

* `git switch feature-navn` Skift til branch

* `git switch -c feature-navn` Opret + skift

* `git branch` Se branches

### 9. Merge en branch ind i main

* `git switch main`

* `git merge feature-navn`

### 10. Se commit-historik

* `git log --oneline` Kort historik

* `git log` Fuld historik

### 11. Undo og reset (mest brugt)

* `git restore --staged filnavn.py` Fjern fil fra staging

* `git restore filnavn.py` Tilbagefør ændringer i fil

### 12. Klon et GitHub-repo

* `git clone git@github.com:larsgam/repo.git`

### 13. Sæt main som default branch (hvis projekt starter med master)

* `git branch -M main`

### 14. Se forskelle

* `git diff`

---

# 
