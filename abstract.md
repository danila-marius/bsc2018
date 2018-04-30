Abstract
--------

    Se doreste proiectarea si antrenarea unei retele neuronale cu scopul de a genera 
retele de sortare optimale. Abstractizand, putem vizualiza o retea de sortare ca pe
o lista ordonata de comparatori (sau swapuri) pe care le aplicam celor `n` fire 
din retea. Modul in care se poate rezolva aceasta problema conceperea unei retele
pe arhitectura NTM antrenata pe swapuri extrase de la mai multi algoritmi de sortare.
Practic, rulam mai multi algoritmi de sortare, pe siruri random de lungime variabila
si salvam swapurile executate de acel algoritm. Odata avute aceste liste de swapuri,
devin ele devin date de antrenament pentru reteaua amintita mai sus. Modelul, va
invata practic sa execute swapurile ca in unul din algoritmii pe care a fost antrenat.

Arhitectura NTM ("Neural Turing Machine") este perfecta pentru acest fel de task pentru
ca sunt optimizate sa invete un algoritm. Diferit de retelele neuronale clasice este faptul
ca acest tip de retele sunt optimizate pe input/output de marime variabila. Astfel putem sa
folosim liste de numere de lungime variabila si de faptul ca numarul de swapuri necesar pentru
a sorta o lista de numere de lungime `k` nu este mereu acelasi.

Spre deosebire de abordarea in care foloseam un algoritm genetic, avantajul aici este ca cea mai
mare parte din timp este investita la antrenarea modelului, predictia fiind cu mult mai rapida
decat executarea unui algoritm genetic.
