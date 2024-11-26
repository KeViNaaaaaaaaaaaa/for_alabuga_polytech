backend-1  | Process SpawnProcess-27:
backend-1  | Process SpawnProcess-28:
backend-1  | Traceback (most recent call last):
backend-1  | Traceback (most recent call last):
backend-1  |   File "/usr/local/lib/python3.12/multiprocessing/process.py", line 314, in _bootstrap
backend-1  |     self.run()
backend-1  |   File "/usr/local/lib/python3.12/multiprocessing/process.py", line 108, in run
backend-1  |     self._target(*self._args, **self._kwargs)
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/_subprocess.py", line 80, in subprocess_started
backend-1  |     target(sockets=sockets)
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/supervisors/multiprocess.py", line 63, in target
backend-1  |     return self.real_target(sockets)
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/server.py", line 65, in run
backend-1  |     return asyncio.run(self.serve(sockets=sockets))
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/asyncio/runners.py", line 194, in run
backend-1  |     return runner.run(main)
backend-1  |            ^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/asyncio/runners.py", line 118, in run
backend-1  |     return self._loop.run_until_complete(task)
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "uvloop/loop.pyx", line 1518, in uvloop.loop.Loop.run_until_complete
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/server.py", line 69, in serve
backend-1  |     await self._serve(sockets)
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/server.py", line 76, in _serve
backend-1  |     config.load()
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/config.py", line 434, in load
backend-1  |     self.loaded_app = import_from_string(self.app)
backend-1  |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/importer.py", line 22, in import_from_string
backend-1  |     raise exc from None
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/importer.py", line 19, in import_from_string
backend-1  |     module = importlib.import_module(module_str)
backend-1  |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/importlib/__init__.py", line 90, in import_module
backend-1  |     return _bootstrap._gcd_import(name[level:], package, level)
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "<frozen importlib._bootstrap>", line 1387, in _gcd_import
backend-1  |   File "<frozen importlib._bootstrap>", line 1360, in _find_and_load
backend-1  |   File "<frozen importlib._bootstrap>", line 1331, in _find_and_load_unlocked
backend-1  |   File "<frozen importlib._bootstrap>", line 935, in _load_unlocked
backend-1  |   File "<frozen importlib._bootstrap_external>", line 995, in exec_module
backend-1  |   File "<frozen importlib._bootstrap>", line 488, in _call_with_frames_removed
backend-1  |   File "/usr/local/lib/python3.12/multiprocessing/process.py", line 314, in _bootstrap
backend-1  |     self.run()
backend-1  |   File "/app/app/main.py", line 6, in <module>
backend-1  |     from app.api.main import api_router
backend-1  |   File "/app/app/api/main.py", line 3, in <module>
backend-1  |     from app.api.routes import login, users, utils, project
backend-1  |   File "/usr/local/lib/python3.12/multiprocessing/process.py", line 108, in run
backend-1  |     self._target(*self._args, **self._kwargs)
backend-1  |   File "/app/app/api/routes/login.py", line 14, in <module>
backend-1  |     from app.utils import (
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/_subprocess.py", line 80, in subprocess_started
backend-1  |     target(sockets=sockets)
backend-1  |   File "/app/app/utils.py", line 7, in <module>
backend-1  |     import emails  # type: ignore
backend-1  |     ^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/supervisors/multiprocess.py", line 63, in target
backend-1  |     return self.real_target(sockets)
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/server.py", line 65, in run
backend-1  |     return asyncio.run(self.serve(sockets=sockets))
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/asyncio/runners.py", line 194, in run
backend-1  |     return runner.run(main)
backend-1  |            ^^^^^^^^^^^^^^^^
backend-1  | ModuleNotFoundError: No module named 'emails'
backend-1  |   File "/usr/local/lib/python3.12/asyncio/runners.py", line 118, in run
backend-1  |     return self._loop.run_until_complete(task)
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "uvloop/loop.pyx", line 1518, in uvloop.loop.Loop.run_until_complete
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/server.py", line 69, in serve
backend-1  |     await self._serve(sockets)
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/server.py", line 76, in _serve
backend-1  |     config.load()
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/config.py", line 434, in load
backend-1  |     self.loaded_app = import_from_string(self.app)
backend-1  |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/importer.py", line 22, in import_from_string
backend-1  |     raise exc from None
backend-1  |   File "/usr/local/lib/python3.12/site-packages/uvicorn/importer.py", line 19, in import_from_string
backend-1  |     module = importlib.import_module(module_str)
backend-1  |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "/usr/local/lib/python3.12/importlib/__init__.py", line 90, in import_module
backend-1  |     return _bootstrap._gcd_import(name[level:], package, level)
backend-1  |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
backend-1  |   File "<frozen importlib._bootstrap>", line 1387, in _gcd_import
backend-1  |   File "<frozen importlib._bootstrap>", line 1360, in _find_and_load
backend-1  |   File "<frozen importlib._bootstrap>", line 1331, in _find_and_load_unlocked
backend-1  |   File "<frozen importlib._bootstrap>", line 935, in _load_unlocked
backend-1  |   File "<frozen importlib._bootstrap_external>", line 995, in exec_module
backend-1  |   File "<frozen importlib._bootstrap>", line 488, in _call_with_frames_removed
backend-1  |   File "/app/app/main.py", line 6, in <module>
backend-1  |     from app.api.main import api_router
backend-1  |   File "/app/app/api/main.py", line 3, in <module>
backend-1  |     from app.api.routes import login, users, utils, project
backend-1  |   File "/app/app/api/routes/login.py", line 14, in <module>
backend-1  |     from app.utils import (
backend-1  |   File "/app/app/utils.py", line 7, in <module>
backend-1  |     import emails  # type: ignore
backend-1  |     ^^^^^^^^^^^^^
backend-1  | ModuleNotFoundError: No module named 'emails'


