Grid
===============

.. figure:: static/res_img/grid_elem.jpeg
   :width: 450pt
   :name: grid_elem

   Elemente de baza in grid

Gridul este frecvent folosit in aplicatii pentru vizualizare, cautare, adaugare sau modificare informatii. Indiferent de natura informatiei, modul de utilizare al gridului, e acelasi. In general, gridul e atasat unui tabel din baza de date. Presupunand ca tabelul contine 100000 randuri, niciodata nu vor fi aduse in browser toate randurile. Filtrarile si paginatia se executa la nivelul serverului astfel incat in browser, la un moment dat e adusa o singura pagina (10,20,50 sau 300 randuri).

.. csv-table:: Semnificatie elemente grid
   :widths: 15 30
   
   "**(1)** Denumire grid","Numele gridului, informatii generale despre grid."
   "**(2)** Denumiri coloane","Nume coloane, click pe zona, sorteaza ascendent sau descendent informatia in grid."
   "**(3)** Filtru rapid","Cauta in coloana dupa conditia `contine`. **Enter** initiaza cautarea. Pentru a anula efectul filtrului pe o coloana, se goleste continutul campului de filtrare. Cautarea e independenta de marimea literei(a sau A)."
   "**(4)** Zona de marcare","Acolo unde aceasta coloana exista, se pot marca in mod independent randuri dintr-o pagina pentru ca ulterior sa se execute bulk (la gramada) o actiune specifica (ex. modifica continutul unei coloane pentru toate randurile marcate.)"
   "**(5)** Rand selectat","Spre deosebire de randurile marcate, intr-un grid poate sa existe un singur rand selectat. Daca dorim sa executam o actiune la nivelul unui rand, il selectam dupa care initiem actiunea (ex. modifica sau sterge rand)"

.. csv-table:: 
   :widths: 15 30

   "**(6)** Zona cu butoane","Zona ce permite actiuni in grid. De la stanga la dreapta, rolul butoanelor este:
   
       - Adauga rand nou.
       - Editeaza randul selectat.
       - Vizualizeaza randul selectat.
       - Sterge randul selectat.
       - Cautare complexa.
       - Reinitializeaza grid(anuleaza orice filtru si reincarca gridul)
       - Rearanjeaza coloane. Coloanele pot fi modificate ca pozitie si/sau ascunse. O data modificata structura gridului, se pastreaza pana la inchiderea aplicatiei (tabului).
       - Export .xls. Randurile filtrate pot fi exportate in format xls. Primul rand reprezinta numele coloanei. Exportul e limitat la maxim 10000 randuri."
   "**(7)** Paginatie","In exemplul din figura, citim din zona de paginatie: Gridul contine 2 pagini, se arata pagina 1, paginile contin maxim 10 randuri. Se poate modifica numarul paginii dorite, numarul de randuri pe pagina. Se poate naviga rand cu rand in ambele directii sau direct la prima/ultima pagina."
   "**(8)** Total inregistrari","Numarul inregistrarilor(dupa filtrare) care pot fi vazute in grid. In figura, numarul este 14."





   