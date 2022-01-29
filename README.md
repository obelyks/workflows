# Project to test Git workflows

And how the results will look like on server
    * Git cmd line
    * A to same v intellij
    * Vybrat si jeden jazyk
    * A vsechno psat v nem/ nemixovat to

## Local Branch

 * Vytvorit local branch
 * Nekolik Commitu v LB
 * potom to dostat nejak do master jako jeden commit

Git commandline

    #napred to vsechno commitovat do vetve 
    git checkout -b novevetevname
    
    git checkout master
    #(tady asi udelat git pull?)
    git merge --squash yourBranch
    git commit

Stejne mi to vytvori merge branchmaster commit automaticky


Jde se vubec nejak zbavit merge commitu?
    
    Merge branch 'master' of https://github.com/obelyks/workflows


## Neco Dalsiho 



    Password for 'https://obelyks@mail.com@github.com':
    remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
    remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
    fatal: Authentication failed for 'https://github.com/obelyks/workflows.git/'


    vpravonahore/otevrit menu/Settings/Vlevodole <> Developers settings/ Personal Access Tokens/Generate New
    sam pro sebe zaskrtnout vsechno/ expiration asi taky na nekonecno

    TODO kam to dat abych to nemusel zapisovat dokola?
    git push https://<GITHUB_ACCESS_TOKEN>@github.com/<GITHUB_USERNAME>/<REPOSITORY_NAME>.git


## Pokus s rebase vs merge na lokalni vetvi
    1. rebase
        - udelat vetev
        - zmeny na vetvi/commit
        - zmeny na main/commit/push
        - zmeny na vetvi/commit
        ---
        - rebase na vetvi (z origin/master: nemusi predtim delat fetch) / po rebase s commit nedela!!!
        - prepnuti na main / pull (melo by tam byt cisto!)
        - merge rebasenute vetve do mainu pres merge(suqash)+comit+push
        -a tedka tam ten merge branch commit neni
        TOsame pres INTELLIJ jestl neni zbytecne chytra a necaje prikazy si tam neprida sama!
            a taky by me zajimalo jak zvlada ty squash merge-treba to bude lepsi
            neni: je to stejne, jenom nenabizi pri commitu po squash vsechny commit
                 messages: ale zase jsou videt v graficke historii (git log)
    2. merge
        - stejne pripravit pripad jako pro rebase
            -vetev->comitnavetvi->comit+pushnamainu->commit na vetvi
        -----
        udelat merge z origin/master (zase abych nemulel fetchovat a delat to z lokalniho msteru)
        comitnout ten merge do vetve
        prepnout se do masteru a udelat squishe merge + comit +push

## Stash a shelve/f
defaultne to ty  ulozene veci nemaze/ale to ani stash kdyz ho pouzivam pres UI
asi pouzije apply misto pop  resp POP STASH checkbox neni puvodne zaskrtnuty
* Shelve je od intellij a vubec neni neni v gitu (funkce je podobna)

###git stash
Tohle by mohlo asi vyresit problemy z lokalnima zmenama ktere nechci komitovat ani mergovat!
muzu je mit v jinem changelistu, ale stejne je radsi stashovat pred pullem
nebo jenom jestli mi zahlasi ze tam nejaky problem je!!!


* git stash push .. ulozi tracked files nekam k pozdejsimu pouziti
                    .. a dalsi a dalsi a dalsi za sebou
* git stash pop .. vyvola zmeny a vymaze
* git stash push -m jmenoslotu   ... asi ale funguje stejne a pri pop se vyvola kdyz je narade(vyzkouset)
* git stash ... bez niceho je jako "git stash push"
* git stash apply cislo.... aplikuje z historie ale necha ji tam
* git stash pop cislo... vyberu si ktery slot ale ten smaze
* git stash list
* git stash show ... list of files -p taky preview co v nich je
* --all  ... i untracked files se ulozi


## Konec
    Ten rebase pres cmd line funguje jak chci
    Merge by mela teoreticky mit o jeden comit navic v lokalni vetvi: a v masteru
    uz vypadat stejne jako rebase pripad

    Merge je horsi protoze mi tam nefungovalo git merge origin/master
    kdyz se master zmenil jinde, ani pres command line ani pres klikani v intellij
    proc? mozna to opravi nejake nastaveni ????

