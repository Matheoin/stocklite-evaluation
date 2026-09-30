# Réponses — chasse au trésor

<!-- Format imposé, une réponse par ligne :
Q01: <réponse>
commande: <commande(s) utilisée(s)>
-->

Q01: il y a 32 commits accessibles depuis le tag depart
commande: git rev-list --count depart

Q02: C'est Sarah Benali qui a écrit la ligne return de la fonction formaterLigne dans src/format.js
commande: git blame depart -- src/format.js

Q03: Voici le SHA du premier commit fautif : 4459c91715f9b1c97cf4776ad2e5afbdb3aa7051
commande: node scripts/controle-alertes.js
          echo $?
          git bisect start
          git bisect bad depart
          git bisect good v0.2.0
          git bisect run node scripts/controle-alertes.js

Q04: API_KEY=sk_live_01de6ba0c9f4d846
commande: git log --all -p -i -G"api[_-]?key|secret|token" --format="COMMIT %h %s"

Q05: 11544ab
commande: git log --all --diff-filter=D --name-only --format="COMMIT %h %s"

Q06: 17 commits sont accessibles depuis la v1.0.0 mais pas depuis v0.2.0 
commande: git rev-list --count v0.2.0..v1.0.0

Q07: c'est le commit "essai-perf" qui est un tag leger
commande: git for-each-ref refs/tags --format="%(refname:short) %(objecttype)"


Q08: 
commande: 

Q09: 
commande: 

Q10: 
commande: 

Q11: 
commande: 

Q12: 
commande: 

Q13: 
commande: 

Q14: 
commande: 

Q15: 
commande: 
