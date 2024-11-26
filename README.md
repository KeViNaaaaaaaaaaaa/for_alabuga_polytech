jenia@jenia-MaiBook-M:~/PycharmProjects/TaskDock$ docker-compose up --build
[+] Building 1.2s (13/13) FINISHED                                                                                                                                                                          docker:default
 => [backend internal] load build definition from Dockerfile                                                                                                                                                          0.0s
 => => transferring dockerfile: 1.03kB                                                                                                                                                                                0.0s
 => [backend internal] load metadata for ghcr.io/astral-sh/uv:0.4.15                                                                                                                                                  1.0s
 => [backend internal] load metadata for docker.io/library/python:3.12                                                                                                                                                0.6s
 => [backend internal] load .dockerignore                                                                                                                                                                             0.0s
 => => transferring context: 116B                                                                                                                                                                                     0.0s
 => [backend stage-0 1/5] FROM docker.io/library/python:3.12@sha256:f71437b2bad6af0615875c8f7fbeeeae1b73e3c76b82056d283644aca5afe355                                                                                  0.0s
 => [backend internal] load build context                                                                                                                                                                             0.0s
 => => transferring context: 4.41kB                                                                                                                                                                                   0.0s
 => [backend] FROM ghcr.io/astral-sh/uv:0.4.15@sha256:0e3e0ce333158c079541f6d59299e78b65aafff7db7111aa7f0f7f8edea520f4                                                                                                0.0s
 => CACHED [backend stage-0 2/5] WORKDIR /app                                                                                                                                                                         0.0s
 => CACHED [backend stage-0 3/5] COPY --from=ghcr.io/astral-sh/uv:0.4.15 /uv /bin/uv                                                                                                                                  0.0s
 => CACHED [backend stage-0 4/5] COPY requirements.txt .                                                                                                                                                              0.0s
 => [backend stage-0 5/5] COPY . .                                                                                                                                                                                    0.0s
 => [backend] exporting to image                                                                                                                                                                                      0.0s
 => => exporting layers                                                                                                                                                                                               0.0s
 => => writing image sha256:a41cedddaf21c020610229d65241f76d53216235d0db0008a3cfde98102a1070                                                                                                                          0.0s
 => => naming to docker.io/library/backend:latest                                                                                                                                                                     0.0s
 => [backend] resolving provenance for metadata file                                                                                                                                                                  0.0s
[+] Running 2/2
 ✔ Container taskdock-db-1       Created                                                                                                                                                                              0.0s 
 ✔ Container taskdock-backend-1  Recreated                                                                                                                                                                            0.1s 
Attaching to backend-1, db-1
db-1       | 
db-1       | PostgreSQL Database directory appears to contain a database; Skipping initialization
db-1       | 
db-1       | 2024-11-26 20:28:09.032 UTC [1] LOG:  starting PostgreSQL 12.22 (Debian 12.22-1.pgdg120+1) on x86_64-pc-linux-gnu, compiled by gcc (Debian 12.2.0-14) 12.2.0, 64-bit
db-1       | 2024-11-26 20:28:09.032 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
db-1       | 2024-11-26 20:28:09.032 UTC [1] LOG:  listening on IPv6 address "::", port 5432
db-1       | 2024-11-26 20:28:09.034 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
db-1       | 2024-11-26 20:28:09.056 UTC [27] LOG:  database system was shut down at 2024-11-26 20:27:34 UTC
db-1       | 2024-11-26 20:28:09.066 UTC [1] LOG:  database system is ready to accept connections
Gracefully stopping... (press Ctrl+C again to force)
Error response from daemon: failed to create task for container: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: exec: "uvicorn": executable file not found in $PATH: unknown
