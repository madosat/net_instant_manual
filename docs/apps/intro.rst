Introducere
===========

**Net-Instant** este un serviciu web, SaaS(software as a service), care s-a născut ca urmare a cererii pe piata de securitate din Romania. Este un dispecerat national, care incearca sa fie un raspuns la urmatoarea intrebare:

**Cum pot aduna mesajele provenite de la centrale diferite (diferiti producatori), transmise de catre comunicatoare diverse (modele, protocoale diferite), intr-o baza de date unica, centralizata ?**

**Net-Instant** reuseste sa faca acest lucru si chiar mai mult, respectand cateva principii:

 - Siguranta si stabilitate in functionare.
 - Viteza mare de raspuns, in conditiile prelucrarii unui volum mare de date.
 - Interfata simpla, prietenoasa cu utilizatorul final.
 - Compatibilitate cu centralele si comunicatoarele de pe piata.
 - Interconectare usoara cu alte servicii SaaS, cum ar fi: SMS, Localizare GPS, etc.
 - Dezvoltabilitate rapida, sigura si usor de implementat. Acest principiu, pe care-l respecta **Net-Instant**, credem ca este cel mai puternic atu al serviciului in acest moment, in competitia cu alte produse similare.

In cadrul companiei de securitate, beneficiarii directi ai serviciului sunt:

 - Dispecerii.
 - Sefii de dispecerate.
 - Echipa tehnica.

.. figure:: static/res_img/topo.png
   :alt: Arhitectura sistem
   :name: arhitectura_sistem

   Arhitectura sistem

Arhitectura sistemului, contine:

 - **Serverul principal**. Sistem de operare Linux, Ubuntu Server. Limbajul folosit pentru implementare: Python. Baza de date poate fi MySQL, Oracle, PostgreSQL.
 - **Serverul de backup**. Serviciul e instalat pe un al doilea server. Acesta functioneaza permanent si sta in sincron cu serverul principal. In momentul cand serverul principal nu mai e functional, evenimentele se trimit catre serverul de backup.
 - **Statiile de lucru**, PC-uri obisnuite, pe care trebuie sa ruleze un browser modern, Chrome sau Firefox. Sistemul de operare poate fi Ubuntu Desktop. In fig.1 statiile de lucru sunt grupate in doua dispecerate, din care unul este dispecerat master.
 - **Unul sau mai multe dispozitive de afisare**, practic sunt televizoare inteligente, capabile sa interogheze periodic serverul si sa afiseze informatii utile in timp real (ex.: deplasarea echipajelor catre obiective).
 - **Receptoare**, respectiv, unitati independente, capabile sa receptioneze mesajele de la diferite tipuri de comunicatoare si sa le aduca intr-un format unitar. Receptoarele se cupleaza TCP cu serverul pentru transmitere mesaje. Au capacitatea de a redirectiona mesajele catre serverul de backup, daca serverul principal nu functioneaza. Legatura intre receptoare si server e bilaterala. Receptarele sunt capabile sa primeasca mesaje de la server pentru interogare obiective.

