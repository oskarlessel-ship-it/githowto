GitHowTo harjutus: repositoorium githowto

Lühike õpiprojekt, kus harjutasin Giti põhitöövoogu päris failide ja commitide peal. Repositooriumis on GitHowTo tuuri käigus tehtud leht index.html ja sellele hiljem lisatud style.css. Eesmärk ei ole valmis veebirakendus, vaid arusaam, kuidas iga väike muudatus liigub töökataloogist commit’i ja sealt GitHubi.

Selle README kirjutasin nii, et teine inimene saaks ilma juhendit avamata aru, millega tegu on, mida ma õppisin ja milliseid käske päriselt kasutasin. Juhend, mille järgi harjutasin, on GitHowTo.

Mis projektiga on tegemist?

GitHowTo on praktiline tuur: iga samm tehakse ise ära. Mina tegin selle repositooriumis oskarlessel-ship-it/githowto. Alguses oli tühi projekt, siis lisasin tavalise HTML-lehe, pealkirja, lõigu ja meta-info. Pärast seda lisasin eraldi stiilifaili ja sidusin selle lehega.

Commitide ajalugu näitab seda sammu-sammult:





Initial commit



Added h1 tag



Added standard HTML page tags



Added HTML header



Added paragraph



Added meta title



Added css stylesheet



Included stylesheet into hello.html

Eraldi vaatasin kahte GitHub Skills kursust, et sama töö oleks GitHubis loetav ja et ma saaksin muudatuse haru kaudu sisse viia:





Introduction to GitHub — repositoorium, haru, commit ja pull request.



Communicate using Markdown — pealkirjad, loendid, lingid, kood ja märkeruudud.

Mida ma projekti käigus õppisin?

Kõige olulisem eristus oli kolme ala vahel. Töökataloog on see, mida ma failides näen. Staging-ala on see, mille ma olen järgmisesse committi valinud. Repositoorium on commitide ajalugu, mis jääb alles ka siis, kui tööfaili hiljem muudan.

HTML-i ja CSS-i lahku hoidmine tegi selle eriti selgeks. style.css lisamine ja selle ühendamine index.html failiga olid kaks eraldi muudatust ja said ka kaks eraldi committi. Nii on hiljem git log abil näha, kumb samm mida muutis.

Õpitud teemad





Repositooriumi loomine ja peidetud .git kaust, kuhu ajalugu salvestub.



Oleku kontroll enne iga salvestamist, et commit’i ei satuks juhuslik fail.



Muudatuse ja faili erinevus: Git jälgib sisu muutust, mitte ainult failinime.



Staging ja commit kahesammulise töövoona, koos lühikese commitsõnumiga.



Ajaloo vaatamine käsuga git log, et näha, mis järjekorras leht valmis sai.



Harud: eraldi tööliin, mida saab hiljem põhiharuga kokku panna.



Haru vahetamine ja liitmine, ning miks konflikt tekib, kui sama kohta on muudetud kahes harus.



Vana seisu taastamine ja kohaliku, veel commitimata muudatuse tühistamine.



GitHub kui kaugrepositoorium: commit ei ole veel jagatud, kuni see on üles laetud.



Markdown, et sama repositooriumi README oleks teisele lugejale arusaadav.

Kuidas Giti põhitöövoog toimib?

Tavaline ring on lühike. Kõigepealt vaatan, mis on muutunud. Siis valin, mis läheb kaasa. Siis salvestan seisu sõnumiga, mida ma ise hiljem mõistan. Kui töö on jagamiseks valmis, lükkan selle GitHubi.

git status
git add index.html style.css
git commit -m "Included stylesheet into hello.html"
git log --oneline
git push

git status näitab, kas fail on jälgimata, muudetud või juba staging-alal. git add ei salvesta ajalukku, vaid märgib muudatuse järgmise commiti jaoks. git commit teeb püsiva seisu. git push viib selle seisu GitHubi, kust õpetaja linki avades tulemuse näeb.

Inline-näide igapäevasest kontrollist: enne commit’i käivitan git status, et näha, kas staging-alal on ainult see fail, mida tahtsin salvestada.

Kui muudatus on katsetus, teen enne haru. Seda mustrit õppisin GitHubi sissejuhatuses: haru, commit, pull request, merge.

git switch -c readme-taiendus
git add README.md
git commit -m "Kirjelda õpitud Git-töövoog README-s"
git push -u origin readme-taiendus

Milliseid Git-käske kasutasin?







Käsk



Mida ma sellega tegin





git init



Tegin projektikaustast Giti repositooriumi





git status



Kontrollisin, mis on muutunud ja mis on juba staging-alal





git add



Valisin index.html või style.css järgmise commiti jaoks





git commit



Salvestasin valitud seisu lühikese sõnumiga





git log



Vaatasin kaheksat committi, millega leht valmis sai





git branch



Lõin ja vaatasin harusid





git switch



Vahetasin haru, et katsetus ei rikuks põhiharu





git merge



Tõin haru töö tagasi põhiharusse

Vanemates juhendites on haru vahetamiseks sageli git checkout. Selles projektis kasutasin uuemat git switch, sest käsu nimi ütleb kohe, et tegu on haru vahetamisega, mitte faili taastamisega.
