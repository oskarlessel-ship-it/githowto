Lühike õpiprojekt, kus harjutasin Giti põhitöövoogu. Repositooriumis on leht `index.html` ja stiilifail `style.css`. Eesmärk oli aru saada, kuidas muudatus liigub failist commit’i ja sealt GitHubi. Juhend oli GitHowTo
## Mida ma õppisin?

Kõige tähtsam oli kolme ala erinevus. Töökataloog on see, mida ma failis näen. Staging-ala on see, mille valin järgmise commiti jaoks. Repositoorium on salvestatud ajalugu.

Õpitud teemad:

- repositooriumi loomine ja peidetud `.git` kaust
- oleku kontroll enne salvestamist
- `git add` ja `git commit` kahesammulise töövoona
- ajaloo vaatamine käsuga `git log`
- haru loomine, vahetamine ja liitmine
- commit’i üleslaadimine GitHubi

## Kuidas töövoog toimib?

Enne iga salvestamist vaatan olekut käsuga `git status`. Siis valin failid, salvestan seisu ja lükkan selle GitHubi.

```bash
git status
git add index.html style.css
git commit -m "Included stylesheet into hello.html"
git log --oneline
git push


Tõin haru töö tagasi põhiharusse

Vanemates juhendites on haru vahetamiseks sageli git checkout. Selles projektis kasutasin uuemat git switch, sest käsu nimi ütleb kohe, et tegu on haru vahetamisega, mitte faili taastamisega.
