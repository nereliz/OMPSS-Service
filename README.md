OMPSS-Service
==============

Internetinio matematinio programavimo ir projektavimo serverines paslaugos diegimo i *OpenStak* debesies platforma 
skriptai. Sis projektas neturi minetos serverines paslaugos iseities kodu. 

Internetinio matematinio programavimo ir projektavimo serverines paslaugos projekta galima rasti pasinaudojus 
sia nuoroda: https://github.com/nereliz/OMPSS-Server

Diegimas:
--------------

Sukurkite aplanka *~/src/juju/charms/precise*

    mkdir ~/src/juju/charms/precise

Tada i naujaji aplanka klonuokite projekta
    
    cd ~/src/juju/charms/precise
    git clone https://github.com/nereliz/OMPSS-Service.git ompss

Po to parsiusta paslauga ikeliamae i debesi

    cd ~/src/juju/charms/
    juju deploy --num-units $n --repository . local:precise/ompss
    
**$n** mazgu skaicius. Mazgu skacius gali buti didesnis negu prijungtu laisvu masinu skaicius, tokiu atveju naujai 
prijungtoms masinos automatiskai bus paskirta si paslauga.



Konfiguravimas:
--------------

Vienintelis galimas konfiguravimas tai *NFS* paslaugos palaikymo igalinimas. Ir *NFS* serverio IP adreso nustatymas.
Jeigu *NFS*paslauga nera igalinta IP adresas bus ignoruojamas.

Pastaba:
-------

Jeigu *NFS* sistemoje bus patalpinta rinkmena pavadinimu *config.ini* tada severines paslaugos konfiguracinis failas
bus pakeistas naujuoju. Tokiu budu bus galima suvienodinti visu darbiniu mazgu nustatymus.

Copyright (c) 2010 - 2013 Nerijus Barauskas

Projektas realizuotas kaip dalis baigimojo magistraturos darbo Siauliu Universitete.
