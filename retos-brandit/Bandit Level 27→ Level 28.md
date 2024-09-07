## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.
## Datos de acceso al nivel
bandit27
**Contraseña**: upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
## Solución
```bash
bandit27@bandit:~$ mktemp -d
/tmp/tmp.Z9EDM81fIi
bandit27@bandit:~$ cd /tmp/tmp.Z9EDM81fIi
bandit27@bandit:/tmp/tmp.Z9EDM81fIi$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_


remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.Z9EDM81fIi$ ls
repo
bandit27@bandit:/tmp/tmp.Z9EDM81fIi$ cd repo
bandit27@bandit:/tmp/tmp.Z9EDM81fIi/repo$ ls
README
bandit27@bandit:/tmp/tmp.Z9EDM81fIi/repo$ cat README
The password to the next level is: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN
```

## Notas adicionales
**git clone**: Este comando clona un repositorio Git desde una ubicación remota a tu máquina local.
**`ssh://bandit27-git@localhost:2220`**:
- **`ssh://`**: Indica que la conexión al servidor remoto se hará utilizando el protocolo SSH.
- **`bandit27-git@localhost`**: Especifica que el usuario es `bandit27-git` y el servidor al que te estás conectando es `localhost`, lo que implica que el servidor Git está en tu propia máquina o accesible a través de un túnel SSH.
- **`:2220`**: Especifica que el puerto utilizado es el `2220`, lo cual es un puerto no estándar (el puerto por defecto para SSH es el `22`). Probablemente, el servicio SSH del repositorio está configurado para usar ese puerto.
## Referencias