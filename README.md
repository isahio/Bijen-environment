# Bijen-environment
My own environment!

Ga van de bijenkorf wifi op de bijenkorf-Guest wifi!

Open een Anaconda Prompt terminal en typ:

conda init bash

Dit zorgt ervoor dat jouw terminal klaar is voor het runnen van de commands. Het beste is om de terminal nu af te sluiten en een nieuwe te openen zodat alles correct wordt uitgevoerd.

Je kan de installatie verifiëren door te kijken of je terminal zoiets als (base) voor elke line heeft staan.

Met de nieuwe terminal, run de commands zoals volgt: (BELANGRIJK: niet alles tegelijk maar stap voor stap!!)

curl [https://raw.githubusercontent.com/isahio/bijen-environment/main/environment.env](https://github.com/isahio/Bijen-environment/blob/main/environment.env) > environment.yml

conda install -n base conda-libmamba-solver

conda config --set solver libmamba

conda env create -f environment.yml

(dit onderstaande stukje code hoeft niet altijd)

rm environment.yml

Dit downloadt een beschrijving van welke bibliotheken gedownload en geinstalleerd moeten worden, en installeert de bibliotheken. Daarna verwijderd het de omschrijvingen.

Nu, wanneer je een nieuwe terminal opent kan je het volgende command gebruiken om onze bijen environment te gebruiken :)

conda activate bijen

Optioneel
Om de environment elke keer te gebruiken als je een nieuwe (Anaconda) terminal opent, doen we als volgt:

echo 'conda activate bijen' >> ~/.bash_profile

We moeten nu nog twee opdrachten uitvoeren, die ervoor zullen zorgen dat Python en sqlite naar behoren functioneren op Windows:

echo "alias python='winpty python'" >> ~/.bash_profile

echo "alias sqlite3='winpty sqlite3'" >> ~/.bash_profile

echo "alias checkpy='winpty checkpy'" >> ~/.bash_profile

Nu, herstart je terminal, en controleer of deze start in de bijen environment.
