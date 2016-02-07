Caracteristici
==============

.. role:: ref

1. Receptie, prelucrare, afisare evenimente [#]_ de la obiective supravegheate.
2. Rutare ID obiectiv, la intrare. Evenimentele de la obiective cu ID-uri diferite, pot fi directionate catre un ID unic.
3. Rutare ID obiectiv, la iesire. Evenimentele primite si directionate catre un obiectiv inregistrat, pot fi retransmise in mod automat, catre un subcontractor pentru dispecerizare dubla.
4. Acces la serviciu pe baza de user si parola cu drepturi diferite in functie de grupul din care face parte utilizatorul. Oricare utilizator, poate sa apartina mai multor grupuri. Grupurile predefinite in sistem sunt:

 - Administrator
 - Editor obiective
 - Dispecer
 - Tehnic
 - Client extern
 - Comun

 Administratorul poate modifica drepturile de acces in aplicatie.

5. Trimite automat sau manual, sms, email, configurabil ca mesaj si forma.
6. Rezolvare incidente [#]_ pe termen scurt, mediu si lung(alarme, lipsa comunicare, lipsa alimentare etc.). Incidentele pe termen scurt (minute) cum ar fi alarmele, se trateaza preluand evenimentul de start. La final, se incheie printr-o rezolutie (ex.: alarma test politie, alarma falsa, alarma reala etc.). Incidentele pe termen mediu (ore) se trateaza prin punerea obiectivului sub urmarire. Aici, dispecerii pot analiza pe baza evolutiei evenimentelor, daca incidentul s-a rezolvat sau nu(lipsa alimentare, lipsa comunicare). In cazul problemelor tehnice, dispecerii creaza :ref:`tickete <ticket>` pe care le preiau echipele tehnice.
7. Evidenta riguroasa, automata a obiectivelor offline, a obiectivelor ramase dezarmate in afara programului.
8. Gestionare echipaje de interventie. Trimitere in misiune pe baza distantei fata de obiectiv, localizarea si urmarirea echipajului pe toata durata misiunii, masurarea precisa a timpului de interventie.
9. :ref:`Sistem de ticketing <ticket>` pentru evidenta si rezolvare probleme in sistem.
10. Generare de rapoarte pentru clienti.
11. Comunicare facila cu personalul tehnic, se trimit email-uri cu atasamente ca:
    
  - ultimele 100 evenimente
  - raport partitii, zone
  - raport utilizatori
  
12. Arhitectura de tip client-server, permite amplasarea serverelor in locatii diferite(pentru siguranta). Dispecerii pot fi localizati in diferite zone, chiar si orase diferite.Tratarea oricarui aspect al dispecerizarii, nu necesita contactul direct intre dispeceri.
 
.. [#] Folosim termenul **eveniment**, pentru orice mesaj trimis de catre comunicator.
.. [#] **Incident**, reprezinta un grup de evenimente consecutive, care incepe cu un eveniment prioritar (prioritate maxima, alarma) si se incheie cu o rezolutie a dispecerului. Pe durata incidentului, dispecerul executa taskuri (trimite echipaje in misiune, discuta cu beneficiar etc.)