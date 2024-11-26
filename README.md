jenia@jenia-MaiBook-M:~/PycharmProjects/TaskDock$ docker-compose up --build
[+] Building 101.2s (11/13)                                                                                                                                                                                 docker:default
 => [backend internal] load build definition from Dockerfile                                                                                                                                                          0.0s
 => => transferring dockerfile: 1.10kB                                                                                                                                                                                0.0s
 => [backend internal] load metadata for ghcr.io/astral-sh/uv:0.4.15                                                                                                                                                  0.2s
 => [backend internal] load metadata for docker.io/library/python:3.12                                                                                                                                                0.6s
 => [backend internal] load .dockerignore                                                                                                                                                                             0.0s
 => => transferring context: 116B                                                                                                                                                                                     0.0s
 => [backend stage-0 1/7] FROM docker.io/library/python:3.12@sha256:f71437b2bad6af0615875c8f7fbeeeae1b73e3c76b82056d283644aca5afe355                                                                                  0.0s
 => [backend internal] load build context                                                                                                                                                                             0.0s
 => => transferring context: 3.19kB                                                                                                                                                                                   0.0s
 => [backend] FROM ghcr.io/astral-sh/uv:0.4.15@sha256:0e3e0ce333158c079541f6d59299e78b65aafff7db7111aa7f0f7f8edea520f4                                                                                                0.0s
 => CACHED [backend stage-0 2/7] WORKDIR /app/                                                                                                                                                                        0.0s
 => CACHED [backend stage-0 3/7] COPY --from=ghcr.io/astral-sh/uv:0.4.15 /uv /bin/uv                                                                                                                                  0.0s
 => [backend stage-0 4/7] COPY ./requirements.txt /backend/                                                                                                                                                           0.0s
 => ERROR [backend stage-0 5/7] RUN --mount=type=cache,target=/root/.cache/pip     pip install --upgrade pip &&     pip install -r requirements.txt                                                                 100.5s
------
 > [backend stage-0 5/7] RUN --mount=type=cache,target=/root/.cache/pip     pip install --upgrade pip &&     pip install -r requirements.txt:
1.459 Requirement already satisfied: pip in /usr/local/lib/python3.12/site-packages (24.2)
16.61 WARNING: Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ReadTimeoutError("HTTPSConnectionPool(host='pypi.org', port=443): Read timed out. (read timeout=15)")': /simple/pip/
32.26 WARNING: Retrying (Retry(total=3, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ReadTimeoutError("HTTPSConnectionPool(host='pypi.org', port=443): Read timed out. (read timeout=15)")': /simple/pip/
48.44 WARNING: Retrying (Retry(total=2, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ReadTimeoutError("HTTPSConnectionPool(host='pypi.org', port=443): Read timed out. (read timeout=15)")': /simple/pip/
65.60 WARNING: Retrying (Retry(total=1, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ReadTimeoutError("HTTPSConnectionPool(host='pypi.org', port=443): Read timed out. (read timeout=15)")': /simple/pip/
84.77 WARNING: Retrying (Retry(total=0, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ReadTimeoutError("HTTPSConnectionPool(host='pypi.org', port=443): Read timed out. (read timeout=15)")': /simple/pip/
99.95 WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager, possibly rendering your system unusable.It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv. Use the --root-user-action option if you know what you are doing and want to suppress this warning.
99.99 
99.99 [notice] A new release of pip is available: 24.2 -> 24.3.1
99.99 [notice] To update, run: pip install --upgrade pip
100.4 
100.4 [notice] A new release of pip is available: 24.2 -> 24.3.1
100.4 [notice] To update, run: pip install --upgrade pip
100.4 ERROR: Could not open requirements file: [Errno 2] No such file or directory: 'requirements.txt'
------
failed to solve: process "/bin/sh -c pip install --upgrade pip &&     pip install -r requirements.txt" did not complete successfully: exit code: 1
