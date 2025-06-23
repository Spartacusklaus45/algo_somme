ALGORITHME SommeDistincte
VAR
   tab1 : TABLEAU[4] D'ENTIER ← [3, 1, 7, 9]
   tab2 : TABLEAU[5] D'ENTIER ← [2, 4, 1, 9, 3]
   i, j : ENTIER
   estCommun : BOOLEAN
   somme : ENTIER
DEBUT
   somme ← 0

   // Parcourir tab1
   POUR i DE 0 À 3 FAIRE
      estCommun ← FAUX
      POUR j DE 0 À 4 FAIRE
         SI tab1[i] = tab2[j] ALORS
            estCommun ← VRAI
         FIN SI
      FIN POUR
      SI estCommun = FAUX ALORS
         somme ← somme + tab1[i]
      FIN SI
   FIN POUR

   // Parcourir tab2
   POUR i DE 0 À 4 FAIRE
      estCommun ← FAUX
      POUR j DE 0 À 3 FAIRE
         SI tab2[i] = tab1[j] ALORS
            estCommun ← VRAI
         FIN SI
      FIN POUR
      SI estCommun = FAUX ALORS
         somme ← somme + tab2[i]
      FIN SI
   FIN POUR

   AFFICHER "Somme des éléments distincts : ", somme
FIN
