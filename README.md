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


## Konec

