<section>
#CLOUD COMPUTING
###Prezentare generala

<small>Creat de catre Adrian Oprea / [@opreaadrian](https://twitter.com/opreaadrian)</small>
</section>

<section>

</section>

Cloud Computing este definit ca fiind folosirea/darea in folosinta a resurselor hardware si software livrate sub forma de serviciu, peste o retea, in speta reteaua Internet. Denumirea de 'cloud computing' are legatura cu reprezentarea retelelor printr-un simbol grafic in forma de nor, in diagramele calcul, si in sistemele de comunicatii ca o abstractizare a infrastructurii complexe pe care o detine/reprezinta o retea in aceste diagrame. Actualmente, cuvantul 'cloud' este folosit ca o reprezentare a Internet-ului, iar prima utilizare a simbolului pentru a reprezenta reteaua Internet dateaza din 1994.

Conceptul fundamental al infrastructurilor de tip 'cloud' dateaza din anii 50', cand mainframe-urile au fost puse la dispozitia universitatilor si corporatiilor cu ajutorul unor calculatoare de tip 'terminal' care nu erau altceva decat niste clienti slabi(thin clients). Dat fiind faptul ca era destul de costisitoare achizitionarea unui 'mainframe', a devenit primordiala gasirea unei modalitati de a obtine maximum de profit in urma unei asemenea investitii, permitandu-le mai multor utilizatori sa partajeze atat accesul fizic/efectiv la calculator cu ajutorul terminalelor cat si partajarea resurselor de procesare, eliminand perioadele de inactivitate ale mainframe-ului, iar acest lucru s-a concretizat in ceea ce industria numea la acea vreme time-sharing.

Prima persoana care a vehiculat termenul de 'cloud computing' a fost Herbert Grosch(autorul [legii lui Grosch](http://en.wikipedia.org/wiki/Grosch%27s_law)), care a sugerat faptul ca lumea intreaga va opera pe terminale 'proaste' sustinute de 15 data-centere mari. Data fiind cheltuiala mare pe care o presupuneau aceste super-calculatoare, mai multe corporatii puteau sa se foloseasca de aceasta putere de calcul prin time-sharing. Printre aceste companii se numara: SBC (The Service Bureau Corporation - 1957), parte a IBM , Tymshare(1966), Dial Data(achizitionata de catre Tymshare in 1968) si multe altele.

In 'cloud computing' serviciilor de la distanta le sunt incredintate datele utilizatorului, soft-urile folosite si calculele/operatiile executate de acestea.

####Tipuri de cloud computing

Exista foarte multe tipuri de 'cloud computing' dintre care am putea enumera:
 
+ IAAS (Ifrastructure As A Service)
+ PAAS (Platform As A Service)
+ SAAS (Software As A Service)
+ NAAS (Network As A Service)
+ STAAS (Storage As A Service)
+ SECAAS (Security As A Service)
+ DAAS (Data As A Service)
+ DAAS (Desktop As A Service)
+ DBAAS (Database As A Service)
+ TEAAS (Test Environment As A Service)
+ APIAAS (API As A Service)
+ BAAS (Backend As A Service)
+ IPAAS (Integration Platform As A Service)

###Amazon Web Services(AWS)

Este o suita de servicii web lansate in Iulie 2002 care constituie o platforma de tip 'cloud computing', oferita de catre Amazon.com prin intermediul retelei Internet. Cele mai cunoscute dintre aceste servicii sunt Amazon EC2 si Amazon S3.

AWS ofera servicii online pentru alte site-uri web sau aplicatii client / care ruleaza pe client in loc sa ruleze pe server. Majoritatea acestor servicii nu sunt expuse direct utilizatorului final ci ofera functionalitati pe care alti dezvoltatori le pot folosi in aplicatiile lor. Serviciile oferite de AWS sunt accesibile peste protocolul [HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) folosind protocoale [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer) si [SOAP](http://en.wikipedia.org/wiki/SOAP_(protocol)). Toate serviciile sunt facturate per-utilizare, dar facturarea se face diferit in functie de serviciu.

###Amazon S3(Simple Storage Service)

Este un serviciu web online de stocare a datelor oferit de catre AWS. Amazon ofera accesul la spatii de stocare prin interfete [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer), [SOAP](http://en.wikipedia.org/wiki/SOAP_(protocol)) si [BitTorrent](http://en.wikipedia.org/wiki/BitTorrent_(protocol)). Amazon S3 a fost lansat public in Statele Unite ale Americii in Martie 2006 si in Europa in Noiembrie 2007.

La inceput, Amazon isi taxa utilizatorii cu $0.15/GB/luna plus costuri suplimentare pentru latimea de banda folosita pentru primirea si trimiterea de date insa de la 1 Noiembrie 2008, preturile s-au diferentiat, mai ales pentru utilizatorii care stocau mai mult de 50 TB, acestia primind discount-uri considerabile.

Amazon sustine ca infrastructura de stocare folosita de catre Amazon S3 este aceeasi cu cea folosita pentru a-si sustine propria retea globala de e-commerce. 


####Progresul companiei:

+ Octombrie 2007 - 10 miliarde de obiecte
+ Ianuarie 2008 - 14 miliarde de obiecte
+ Octombrie 2008 - 29 de miliarde de obiecte
+ Martie 2009 - 52 de miliarde de obiecte
+ August 2009 - 64 de miliarde de obiecte
+ Martie 2010 - 102 de miliarde de obiecte
+ Iunie 2012 - 1 trilion de obiecte

Compania a declarat in Iunie 2012 ca stocheaza mai mult de un trilion de obiecte.
Amazon S3 include gazduire web, gazduire media (imagini, video, etc.) si spatii de stocare pentru sisteme de backup. Oferta include 99.9% uptime garantat, iar acest procent calculat la numarul de minute dintr-o luna inseamna 43 de minute de downtime pe luna.

####Design-ul
Compania nu a facut public design-ul sau implementarea serviciului Amazon S3. S3 stocheaza obiecte arbitrare(fisiere) de pana la 5TB, fiecare fiind acompaniat de catre 2kb de metadata.  Obiectele sunt organizate in 'galeti'(buckets) fiecare dintre acestea fiind detinute/mapate catre un cont AWS si identificate in interiorul container-ului sau printr-o cheie unica. 

Numele 'galetilor' si cheile sunt alese in asa fel incat obiectele sa fie adresabile atat folosind un URL de tipul HTTP cat si atat folosirea metodei [GET](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html) a protocolului [HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol), a protocolului BitTorrent sau prin interfete de tip [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer)/[SOAP](http://en.wikipedia.org/wiki/SOAP_(protocol)):

+ http://s3.amazonaws.com/bucket/key
+ http://bucket.s3.amazonaws.com/key

Dat fiind faptul ca obiectele sunt accesibile de catre clienti HTTP, S3 poate fi utilizat ca inlocuitor al infrastructurii web statice prin servirea de continut (in mare parte continut media), actionand ca un CDN(Content Delivery Network).

####Gazduire web
Din Februarie 2011, Amazon S3 ofera si optiunea de a gazdui site-uri statice cu suport pentru documente de tip index si eroare. Acest suport a fost adaugat datorita unor cereri ce dateaza din anul 2006. Ceea ce nu permite Amazon S3 este maparea catre domenii de tipul `www.foobar.com` ci doar maparea catre subdomenii, de exemplu : `baz.foobar.com`. De fapt, tehnic este posibil insa acest aspect nu este documentat de catre Amazon.

####Moduri de utilizare notabile

Multe sisteme de fisiere bazate pe User Mode File System (FUSE) pentru sisteme de operare UNIX sau asemanatoare cu UNIX care pot fi folosite pentru a atasa o galeata S3 ca fisier de sisteme, insa trebuie avut in vedere faptul ca 'semantica' din spatele sistemului de fisiere al Amazon S3 nu este compatibila cu un sistem de fisiere POSIX, si exista posibilitatea ca sistemul sa nu se comporte conform asteptarilor.

Alte aplicatii de backup sau marketplace-uri care folosesc Amazon S3 sunt: [Dropbox](), [StoreGrid](), [Zmanda](), [Ubuntu One]().

####Competitia
Priza pe care serviciile oferite de S3 a avut-o in randul companiilor si a dezvoltatorilor, a adus cu sine o serie de servicii concurente cu Amazon S3 bazate chiar pe API-ul S3. Aceste servicii folosesc interfata standard insa se diferentiaza prin tehnologiile ce stau in spatele software-ului si modelul de business care le sprijina. Un standard in materie de 'cloud storage' trebuie sa permita furnizorilor de servicii concurente sa isi creeze serviciile si clientii folosind diferite parti in diferite moduri dar sa comunice si sa ofere urmatoarele beneficii:

1. Cresterea concurentei prin oferirea unui set de reguli, care sa interzica monopolizarea pietei de catre companiile mari si sa permita companiilor mai mici sa intre pe piata.
2. Incurajarea inovatiilor
3. Oferirea de solutii prompte si adecvate pentru livrarea functionalitatii, ca raspuns la cererea de pe piata.

####Incheiere
Adoptarea unei tehnologii noi e o provocare. A sti ca sunt servicii concurente pe o piata construita dupa niste standarde face asimilarea si acceptarea aplicatiilor de tip client mult mai usoara. Putem alege propriul furnizor de servicii in functie de locatie, viteza, preturi, cat si unelte/aplicatii care functioneaza cu API-ul furnizorului respectiv.