## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.
Clone the repository and find the password for the next level.
## Datos de acceso al nivel
bandit28
**Contraseña**: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

## Solución
```bash
bandit28@bandit:/tmp/tmp.xCahUsmZ6W$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/tmp.xCahUsmZ6W$ ls
repo
bandit28@bandit:/tmp/tmp.xCahUsmZ6W$ cd repo
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ git log
commit 8cbd1e08d1879415541ba19ddee3579e80e3f61a (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Wed Jul 17 15:57:30 2024 +0000

    fix info leak

commit 73f5d0435070c8922da12177dc93f40b2285e22a
Author: Morla Porla <morla@overthewire.org>
Date:   Wed Jul 17 15:57:30 2024 +0000

    add missing data

commit 5f7265568c7b503b276ec20f677b68c92b43b712
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:30 2024 +0000

    initial commit of README.md
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ git branch
* master
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ git chekout 73f5d0435070c8922da12177dc93f40b2285e22a
git: 'chekout' is not a git command. See 'git --help'.

The most similar command is
        checkout
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ git checkout 73f5d0435070c8922da12177dc93f40b2285e22a
Note: switching to '73f5d0435070c8922da12177dc93f40b2285e22a'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 73f5d04 add missing data
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.xCahUsmZ6W/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
```
## Notas adicionales
**git log:** en Git se utiliza para mostrar el **historial de confirmaciones** (commits) de un repositorio. Este comando lista todas las confirmaciones realizadas en el proyecto, mostrando información como el identificador del commit, el autor, la fecha y el mensaje asociado con cada commit.
**git branch**: en Git se utiliza para gestionar y visualizar las ramas en un repositorio. Las ramas son versiones paralelas del código que te permiten trabajar en diferentes características o correcciones sin afectar la rama principal.
**git checkout**: mueve tu árbol de trabajo (los archivos de tu repositorio) al estado exacto que tenía el repositorio en el commit especificado.
## Referencias
