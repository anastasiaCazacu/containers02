# containers02-

This lab introduced me to the fundamental concepts of containerization and set up my working environment for future projects. It provided a solid understanding of containerization and a foundation for future projects.

## Tema: Prima aplicatie Docker

### Scopul

Acest laborator m-a facut cunoscuta cu conceptele fundamentale ale containerizarii si am configurat mediul meu de lucru pentru proiectele viitoare. Asigura o întelegere solida a containerizarii si o baza pentru proiectele viitoare.

### Sarcina

Am descarcat si am instalat Docker Desktop si am verificat functionalitatea acestuia.

### Descrierea executii lucrarii cu raspunsuri la intrebari

#### Executarea

1. Clonarea repozitoriului pe GITHUB: M-am logat pe contul de GitHub, am creat un nou repozitoriu cu numele "containers02" cu creare a unui fisier README.md bifand in "Initialize this repository with a README".
2. Clonarea repozitoriului pe compiuterul meu: Am clonat : <https://github.com/anastasiaCazacu/containers02-.git> si am ales locatia clonarii.
3. Creez fisierul Dockerfile fara alta exensie deoarece Docker asa si il recunoaste si inserez continutul propus.
4. Creez directorul "site" si fisierul "index.html" cu un continut arbitrar.

#### Pornirea si testarea

- execut `docker build -t containers02 .` a durat:"Building 10.8s (8/8) FINISHED" . "docker build"- initiaza procesul de construire a imaginii Docker. "-t containers02"- eticheteaza imaginea construita cu numele "containers02". Punctul "."- indica ca fisierul "Docker" se afla in directorul curent.
- execut comanda pentru a porni containerul: `docker run --name containers02 containers02`. si se afiseaza "hello from 7a8ce7b0ca5a".
- Execut "docker rm containers02
docker run -ti --name containers02 containers02 bash" -pentru ca containerul il voi sterge si il voi porni din nou. "docker rm containers02"- sterge containerul existent containers02.
    a. Cu "docker run  --name containers02 containers02 bash"- porneste unui container Doker.
    b. "-ti"- de a se executa in -t- terminal si i- in mod interativ.
    c. "--name containers02 containers02"- este numele imaginii Docker- numele este "containers02" si imaginea noua cu acelasi nume.
    d.- "bash"- va fi rulata în interiorul containerului adica un shell bush. Dupa executarea acestei comenzi, un nou container containers02 va fi pornit si vei avea acces la un shell bash în interiorul acestuia
- `root@197edea1759c:/var/www/html# ls -l
total 4
-rwxr-xr-x 1 root root 157 Feb 24 19:57 index.html"- navighez catre "www/html`. "ls -l"- listarea arata ca: fisierul index.html a fost copiat cu succes în containerul Docker. Acesta are permisiunile:"-rwxr-xr-x"
    a. primul caracter "-" merge vorba despre un fisier obisnuit.
    b. primele 3 caractere "rwx"- asigura proprietarul poate citi, modifica si executa fisierul.
    c. urmatoarele 3 caractere"r-x" -membrii grupului de utilizatori poate executa, citi dar nu poate modifica.
    d. toti ceilalti utilizatori (public) "r-x" - poate executa, citi dar nu poate modifica.
    e. si dimensiunea de 157 bytes.
    f. 157- Dimensiunea fisierului în bytes.
    g. Feb 24 19:57- Data si ora ultimei modificari a fisierului.
    h. index.html- numele fisierului.
- cu `exit`- Inchid fereastra cu aceasta comanda. Am inchis cu succes sesiunea interactiva din interiorul containerului Docker.

Urcarea fisierelor pe GitHub :

1. Intru in directoriul curent cu `cd /caleaMea`.
2. Cu `git add .`- adaug fisierele in staging.
3. `git commit -m "Adaug fisierele proiectului containers02"`-
4. `git push origin main`- arunc(urc) modificarile pe GitHub.

### Concluzii

Acest laborator m-a familiarizat cu conceptele de baza ale containerizarii si cu utilizarea Docker. Cu ajutorul lui am configurat mediul de lucru, creat un Dockerfile si am rulata o aplicatie simpla într-un container. Am învatat sa construiasca si sa gestioneze containere Docker,pregatindune pentru provocarile viitoare.

### Bibliografie

<https://docs.docker.com/get-started/introduction/>
<https://learn.microsoft.com/en-us/training/modules/intro-to-docker-containers/>
