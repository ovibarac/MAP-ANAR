# MAP-ANAR

Administrația Națională Apele Române (ANAR) monitorizează periodic în fiecare regiune geografică
cotele medii ale râurilor.
Se cere proiectarea unei aplicații care să emită avertizări în localitățile pentru care cotele reprezintă
pericol redus, pericol mediu sau pericol major de inundații.
1. (1p) La pornirea aplicației se afișează o fereastră în care sunt listate toate râurile și cota lor
medie.
Un râu este reprezentat prin nume și are o cotăMedie
Toate râurile se preiau din fișier/bază de date.
2. (2p) La pornirea aplicației se mai deschide o fereastră cu avertizări.
Există trei tipuri de avertizări:
1. Risc redus de inundații (cota nu depășește nicun prag)
2. Risc mediu de inundații (cota depășește un prag minim de risc)
3. Risc major de inundații (cota depășește un prag maxim admis)
Astfel, se afișează localitățile care se încadrează în unul dintre aceste riscuri.
O localitate se identifică prin nume, râul principal care o tranzitează (un singur râu),
cotaMinimăDeRisc (cmdr) care plasează localitatea într-un risc mediu de inundații dacă este
depășită și cotaMaximăAdmisă (cma) care plasează localitatea în risc major de inundații dacă este
depășită.
Localitățile se preiau din fișier/bază de date.
Fără alte informații, toate localitățile prezintă un risc redus de inundații.
3. (2p) Inginerul poate schimba cota medie a unui râu în fereastra destinată râurilor. Modificarea
devine vizibilă în lista râurilor.
4. (2p) În momentul în care s-a schimbat cota medie a unui râu, în fereastra de avertizări se vor
reorganiza automat localitățile în funcție de riscul la care sunt supuse.
Exemplu:
Râul Arieș ajunge la cota de 6m
Câmpia-Turzii are cmdr de 4m și cma de 10m -> risc mediu de inundații
(s-a depășit cmdr dar nu s-a depășit cma)
Turda are cmdr de 2m și cma de 5m(<6m) -> risc major de inundații (s-a depășit cma)
O localitate este afectată de cota minimă a unui râu doar dacă râul trece prin respectiva
localitate.
Cerinte non-functionale - 2p:
• Procesarea va avea loc numai la nivel de service sau de controller; interacțiunea cu sursa de date se
va face numai prin intermediul repository-ului (puteti folosi baze de date sau fișiere text).
• Interactiunea cu utilizatorul va avea loc numai in UI (GUI).
• Se cere eliminarea codului care nu este folosit, precum și a functionalitatilor care nu s-au cerut (dacă
ați lucrat cu ceva template de la lab).
• Clasele, atributele și metodele lor vor avea exact numele cerute în problema sau nume sugestiv dacă
nu s-a specificat explicit numele lor.
IMPORTANT
• Se punctează doar cerințele funcționale care rulează
• Orice cod care nu poate fi explicat, atrage după sine nepunctarea cerintei/cerințelor din care face
parte
• Nu aveți voie sa comunicati în timpul examenului, în nicio modalitate posibila de a face acest lucru
(chat, mail, …etc.)
Cerințe extra (1p)
1. Localitățile cu risc redus de inundații se vor afișa cu verde, portocaliu risc mediu și roșu
pentru risc major. De asemenea, la selectarea unei localități se afișează râul care o tranzitează
și cota la care se află, alături de limitele cmdr și cma.
2. Posibilitatea de a determina grupa de risc pentru o localitate care nu este înregistrată (se
introduc valorile pentru cmdr și cma și râul care tranzitează) și se afișează un mesaj
corespunzător. Dacă râul nu este înregistrat, se afișează un mesaj de eroare.
