jenia@jenia-MaiBook-M:~/PycharmProjects/TaskDock$ docker-compose up --build
[+] Running 15/1
 ✔ db Pulled                                                                                                                                                                                                         15.2s 
[+] Building 2.9s (12/14)                                                                                                                                                                                   docker:default
 => [backend internal] load build definition from Dockerfile                                                                                                                                                          0.0s
 => => transferring dockerfile: 1.30kB                                                                                                                                                                                0.0s
 => [backend internal] load metadata for docker.io/library/python:3.10                                                                                                                                                2.0s
 => [backend internal] load metadata for ghcr.io/astral-sh/uv:0.4.15                                                                                                                                                  2.6s
 => [backend internal] load .dockerignore                                                                                                                                                                             0.0s
 => => transferring context: 116B                                                                                                                                                                                     0.0s
 => [backend internal] load build context                                                                                                                                                                             0.0s
 => => transferring context: 118.79kB                                                                                                                                                                                 0.0s
 => CANCELED [backend stage-0 1/8] FROM docker.io/library/python:3.10@sha256:941b0bfddbf17d809fd1f457acbf55dfca014e3e0e3d592b1c9070491681bc02                                                                         0.1s
 => => resolve docker.io/library/python:3.10@sha256:941b0bfddbf17d809fd1f457acbf55dfca014e3e0e3d592b1c9070491681bc02                                                                                                  0.0s
 => => sha256:2eb72484c25c39aba019b0ab5679c2436833a0b705e955ed8e13c06ee900dd63 2.33kB / 2.33kB                                                                                                                        0.0s
 => => sha256:941b0bfddbf17d809fd1f457acbf55dfca014e3e0e3d592b1c9070491681bc02 9.08kB / 9.08kB                                                                                                                        0.0s
 => => sha256:0a9be5c27d86b455f9fe577d40bc92f7ca0ef869bd24450b42e5c85469220d43 6.32kB / 6.32kB                                                                                                                        0.0s
 => CANCELED [backend] FROM ghcr.io/astral-sh/uv:0.4.15@sha256:0e3e0ce333158c079541f6d59299e78b65aafff7db7111aa7f0f7f8edea520f4                                                                                       0.1s
 => => resolve ghcr.io/astral-sh/uv:0.4.15@sha256:0e3e0ce333158c079541f6d59299e78b65aafff7db7111aa7f0f7f8edea520f4                                                                                                    0.0s
 => => sha256:0e3e0ce333158c079541f6d59299e78b65aafff7db7111aa7f0f7f8edea520f4 2.19kB / 2.19kB                                                                                                                        0.0s
 => => sha256:8c507bfc088616f51272fde420751dd5d7f2ade22ee328728473917d3401707a 860B / 860B                                                                                                                            0.0s
 => => sha256:5d91b6119c07964caeb85abad8b47af39373bb3f19abc8f389c8223e3e65d8e6 1.49kB / 1.49kB                                                                                                                        0.0s
 => CACHED [backend stage-0 2/8] WORKDIR /app/                                                                                                                                                                        0.0s
 => CACHED [backend stage-0 3/8] COPY --from=ghcr.io/astral-sh/uv:0.4.15 /uv /bin/uv                                                                                                                                  0.0s
 => ERROR [backend stage-0 4/8] RUN --mount=type=cache,target=/root/.cache/uv     --mount=type=bind,source=uv.lock,target=uv.lock     --mount=type=bind,source=pyproject.toml,target=pyproject.toml     uv sync --fr  0.0s
 => ERROR [backend stage-0 5/8] COPY ./scripts /app/scripts                                                                                                                                                           0.0s
 => ERROR [backend stage-0 6/8] COPY ./pyproject.toml ./uv.lock ./alembic.ini /app/                                                                                                                                   0.0s
------
 > [backend stage-0 4/8] RUN --mount=type=cache,target=/root/.cache/uv     --mount=type=bind,source=uv.lock,target=uv.lock     --mount=type=bind,source=pyproject.toml,target=pyproject.toml     uv sync --frozen --no-install-project:
------
------
 > [backend stage-0 5/8] COPY ./scripts /app/scripts:
------
------
 > [backend stage-0 6/8] COPY ./pyproject.toml ./uv.lock ./alembic.ini /app/:
------
failed to solve: failed to compute cache key: failed to calculate checksum of ref e18cd7a0-7fc7-4c7b-8a98-221e336c7e38::x2v1zw97am4wmf67g4jolnzg8: "/uv.lock": not found
jenia@jenia-MaiBook-M:~/PycharmProjects/TaskDock$ 
