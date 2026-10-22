Prefect collects anonymous usage data to improve the product.
To opt out: set PREFECT_SERVER_ANALYTICS_ENABLED=false on the server, or DO_NOT_TRACK=1 in the client.
Learn more: https://docs.prefect.io/concepts/telemetry

17:19:08.830 | INFO    | prefect - Starting temporary server on http://127.0.0.1:8721
See https://docs.prefect.io/v3/concepts/server#how-to-guides for more information on running a dedicated Prefect server.
17:19:16.206 | ERROR   | docket.dependencies - ↩ [    28ms] send_telemetry_heartbeat(){send_telemetry_heartbeat}
Traceback (most recent call last):
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 1958, in _exec_single_context
    self.dialect.do_execute(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        cursor, str_statement, effective_parameters, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/default.py", line 1192, in do_execute
    cursor.execute(statement, parameters)
    ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 258, in execute
    self._adapt_connection._handle_exception(error)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 412, in _handle_exception
    self._handle_exception_no_connection(self.dbapi, error)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/dialects/sqlite/aiosqlite.py", line 237, in _handle_exception_no_connection
    super()._handle_exception_no_connection(dbapi, error)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 409, in _handle_exception_no_connection
    raise error.with_traceback(exc_info[2])
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 256, in execute
    return await_(self._execute_async(operation, parameters))
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/concurrency.py", line 167, in await_
    return current.parent.switch(awaitable)  # type: ignore[no-any-return]
           ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/concurrency.py", line 205, in greenlet_spawn
    value = await result
            ^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 279, in _execute_async
    result = await self._cursor.execute(operation, parameters)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/cursor.py", line 40, in execute
    await self._execute(self._cursor.execute, sql, parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/cursor.py", line 32, in _execute
    return await self._conn._execute(fn, *args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/core.py", line 160, in _execute
    return await future
           ^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/core.py", line 63, in _connection_worker_thread
    result = function()
sqlite3.OperationalError: database is locked

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/docket/worker.py", line 1134, in _execute
    result = await execution.function(
             ^^^^^^^^^^^^^^^^^^^^^^^^^
        *execution.args, **final_kwargs
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/server/services/telemetry.py", line 80, in send_telemetry_heartbeat
    session_start_timestamp, session_id = await _fetch_or_set_telemetry_session(db=db)
                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/server/services/telemetry.py", line 54, in _fetch_or_set_telemetry_session
    await configuration.write_configuration(session, telemetry_session)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/server/models/configuration.py", line 29, in write_configuration
    await session.flush()
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/ext/asyncio/session.py", line 1030, in flush
    await greenlet_spawn(self.sync_session.flush, objects=objects)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/concurrency.py", line 212, in greenlet_spawn
    result = context.switch(value)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/session.py", line 4543, in flush
    self._flush(objects)
    ~~~~~~~~~~~^^^^^^^^^
  File "<sqlalchemy generated warned() wrapper for sqlalchemy.orm.session.Session._flush>", line 2, in _flush
    return target(fn, self, objects=objects)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/deprecations.py", line 281, in warned
    return fn(*args, **kwargs)  # type: ignore[no-any-return]
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/session.py", line 4686, in _flush
    with util.safe_reraise():
         ~~~~~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/langhelpers.py", line 166, in __exit__
    raise exc_value.with_traceback(exc_tb)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/session.py", line 4647, in _flush
    flush_context.execute()
    ~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/unitofwork.py", line 467, in execute
    rec.execute(self)
    ~~~~~~~~~~~^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/unitofwork.py", line 643, in execute
    util.preloaded.orm_persistence._save_obj(
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        self.mapper,
        ^^^^^^^^^^^^
        uow.states_for_mapper_hierarchy(self.mapper, False, False),
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        uow,
        ^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/persistence.py", line 92, in _save_obj
    _emit_insert_statements(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        base_mapper,
        ^^^^^^^^^^^^
    ...<3 lines>...
        insert,
        ^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/orm/persistence.py", line 1237, in _emit_insert_statements
    result = connection.execute(
        statement,
        params,
        execution_options=execution_options,
    )
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 1463, in execute
    return meth(
        self,
        distilled_parameters,
        execution_options or NO_OPTIONS,
    )
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/sql/elements.py", line 533, in _execute_on_connection
    return connection._execute_clauseelement(
           ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        self, distilled_params, execution_options
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 1683, in _execute_clauseelement
    ret = self._execute_context(
        dialect,
    ...<9 lines>...
        param_dict=param_dict,
    )
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 1837, in _execute_context
    return self._exec_single_context(
           ~~~~~~~~~~~~~~~~~~~~~~~~~^
        dialect, context, statement, parameters
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 1977, in _exec_single_context
    self._handle_dbapi_exception(
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        e, str_statement, effective_parameters, cursor, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 2347, in _handle_dbapi_exception
    raise sqlalchemy_exception.with_traceback(exc_info[2]) from e
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/base.py", line 1958, in _exec_single_context
    self.dialect.do_execute(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        cursor, str_statement, effective_parameters, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/engine/default.py", line 1192, in do_execute
    cursor.execute(statement, parameters)
    ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 258, in execute
    self._adapt_connection._handle_exception(error)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 412, in _handle_exception
    self._handle_exception_no_connection(self.dbapi, error)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/dialects/sqlite/aiosqlite.py", line 237, in _handle_exception_no_connection
    super()._handle_exception_no_connection(dbapi, error)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 409, in _handle_exception_no_connection
    raise error.with_traceback(exc_info[2])
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 256, in execute
    return await_(self._execute_async(operation, parameters))
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/concurrency.py", line 167, in await_
    return current.parent.switch(awaitable)  # type: ignore[no-any-return]
           ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/util/concurrency.py", line 205, in greenlet_spawn
    value = await result
            ^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/sqlalchemy/connectors/asyncio.py", line 279, in _execute_async
    result = await self._cursor.execute(operation, parameters)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/cursor.py", line 40, in execute
    await self._execute(self._cursor.execute, sql, parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/cursor.py", line 32, in _execute
    return await self._conn._execute(fn, *args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/core.py", line 160, in _execute
    return await future
           ^^^^^^^^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/aiosqlite/core.py", line 63, in _connection_worker_thread
    result = function()
sqlalchemy.exc.OperationalError: (sqlite3.OperationalError) database is locked
[SQL: INSERT INTO configuration ("key", value, id, created, updated) VALUES (:key, :value, :id, :created, :updated)]
[parameters: {'key': 'TELEMETRY_SESSION', 'value': '{"session_id": "aebb9db4-f4e9-4d21-b366-444576e28fd4", "session_start_timestamp": "2026-10-22T15:19:16.200292+00:00"}', 'id': '2f443c91-1bd7-42c5-98b4-ed2755a6188a', 'created': '2026-10-22 15:19:16.203161', 'updated': '2026-10-22 15:19:16.203170'}]
(Background on this error at: https://sqlalche.me/e/21/e3q8)
17:19:16.568 | INFO    | Flow run 'furry-quail' - Beginning flow run 'furry-quail' for flow 'Bug Bounty Recon Flow'
17:19:16.573 | INFO    | Flow run 'furry-quail' - === Démarrage du Bug Bounty Recon Flow pour duraline.com ===
17:19:16.584 | INFO    | Flow run 'furry-quail' - Répertoire de sortie: /home/ogaudel/Dev/recon_bot/outputs/duraline_com
17:19:16.642 | INFO    | Task run 'Subdomain Discovery & Live Check-ea8' - Démarrage de la découverte de sous-domaines pour duraline.com
[*] Querying passive sources for duraline.com...
[!] ThreatMiner Error: HTTPSConnectionPool(host='api.threatminer.org', port=443): Read timed out. (read timeout=15)
[*] Launching binary tools (Subfinder, Assetfinder, Amass)...
[+] Total unique subdomains found: 153
[*] Checking for live targets with httpx...
[!] Erreur de httpx: Usage: httpx [OPTIONS] URL

Error: No such option '-l'.
[*] Checking for live targets with technology detection (httpx)...
[*] Filtering for interesting targets (JS/TS frameworks + Auth keywords)...
[!] Warning: info file not found.

--- Done ! Results saved in /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt and /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_info.txt ---
17:21:35.633 | INFO    | Task run 'Subdomain Discovery & Live Check-ea8' - Sous-domaines trouvés: 153 | Cibles live: 0 | Cibles intéressantes: 0
17:21:35.638 | INFO    | Task run 'Subdomain Discovery & Live Check-ea8' - Finished in state Completed()
17:21:35.679 | INFO    | Task run 'Port Scan & Takeover Check-353' - Scan de ports (Naabu) et Subdomain Takeover (Subjack) pour duraline.com
17:21:35.681 | INFO    | Task run 'Port Scan & Takeover Check-353' - Task run failed with exception: FileNotFoundError("[!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.") - Retry 1/1 will start 20 second(s) from now
17:21:55.684 | INFO    | Task run 'Port Scan & Takeover Check-353' - Scan de ports (Naabu) et Subdomain Takeover (Subjack) pour duraline.com
17:21:55.686 | ERROR   | Task run 'Port Scan & Takeover Check-353' - Task run failed with exception: FileNotFoundError("[!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.") - Retries are exhausted
Traceback (most recent call last):
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1030, in run_context
    yield self
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1699, in run_task_sync
    engine.call_task_fn(txn)
    ~~~~~~~~~~~~~~~~~~~^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1047, in call_task_fn
    result = call_with_parameters(self.task.fn, parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/utilities/callables/__init__.py", line 404, in call_with_parameters
    return fn(*args, **kwargs)
  File "/home/ogaudel/Dev/recon_bot/tasks.py", line 48, in port_scan_task
    result = scan_ports_and_takeover(domain, Path(output_dir) if output_dir else None)
  File "/home/ogaudel/Dev/recon_bot/modules/port_scanner.py", line 20, in scan_ports_and_takeover
    raise FileNotFoundError(f"[!] Erreur: {input_file} introuvable. Lance subdomain_recon d'abord.")
FileNotFoundError: [!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.
17:21:55.696 | ERROR   | Task run 'Port Scan & Takeover Check-353' - Finished in state Failed("Task run encountered an exception FileNotFoundError: [!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.")
17:21:56.629 | ERROR   | Flow run 'furry-quail' - Encountered exception during execution: FileNotFoundError("[!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.")
Traceback (most recent call last):
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 1330, in run_context
    yield self
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 2111, in run_flow_sync
    engine.call_flow_fn()
    ~~~~~~~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 1350, in call_flow_fn
    result = call_with_parameters(self.flow.fn, self.parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/utilities/callables/__init__.py", line 404, in call_with_parameters
    return fn(*args, **kwargs)
  File "/home/ogaudel/Dev/recon_bot/orchestrator.py", line 51, in main_recon_flow
    port_res = port_scan_task(domain, output_dir=target_out_dir)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/tasks.py", line 1240, in __call__
    return run_task(
        task=self,
    ...<2 lines>...
        return_type=return_type,
    )
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1932, in run_task
    return run_task_sync(**kwargs)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1702, in run_task_sync
    return engine.state if return_type == "state" else engine.result()
                                                       ~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 622, in result
    raise self._raised
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1030, in run_context
    yield self
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1699, in run_task_sync
    engine.call_task_fn(txn)
    ~~~~~~~~~~~~~~~~~~~^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1047, in call_task_fn
    result = call_with_parameters(self.task.fn, parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/utilities/callables/__init__.py", line 404, in call_with_parameters
    return fn(*args, **kwargs)
  File "/home/ogaudel/Dev/recon_bot/tasks.py", line 48, in port_scan_task
    result = scan_ports_and_takeover(domain, Path(output_dir) if output_dir else None)
  File "/home/ogaudel/Dev/recon_bot/modules/port_scanner.py", line 20, in scan_ports_and_takeover
    raise FileNotFoundError(f"[!] Erreur: {input_file} introuvable. Lance subdomain_recon d'abord.")
FileNotFoundError: [!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.
17:21:56.682 | INFO    | Flow run 'furry-quail' - Finished in state Failed("Flow run encountered an exception: FileNotFoundError: [!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.")
Traceback (most recent call last):
  File "/home/ogaudel/Dev/recon_bot/orchestrator.py", line 138, in <module>
    main_recon_flow(
    ~~~~~~~~~~~~~~~^
        domain=args.domain,
        ^^^^^^^^^^^^^^^^^^^
    ...<3 lines>...
        output_dir=args.output_dir,
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flows.py", line 1887, in __call__
    return run_flow(
        flow=self,
    ...<2 lines>...
        return_type=return_type,
    )
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 2268, in run_flow
    ret_val = run_flow_sync(**kwargs)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 2113, in run_flow_sync
    return engine.state if return_type == "state" else engine.result()
                                                       ~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 788, in result
    raise self._raised
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 1330, in run_context
    yield self
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 2111, in run_flow_sync
    engine.call_flow_fn()
    ~~~~~~~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/flow_engine.py", line 1350, in call_flow_fn
    result = call_with_parameters(self.flow.fn, self.parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/utilities/callables/__init__.py", line 404, in call_with_parameters
    return fn(*args, **kwargs)
  File "/home/ogaudel/Dev/recon_bot/orchestrator.py", line 51, in main_recon_flow
    port_res = port_scan_task(domain, output_dir=target_out_dir)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/tasks.py", line 1240, in __call__
    return run_task(
        task=self,
    ...<2 lines>...
        return_type=return_type,
    )
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1932, in run_task
    return run_task_sync(**kwargs)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1702, in run_task_sync
    return engine.state if return_type == "state" else engine.result()
                                                       ~~~~~~~~~~~~~^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 622, in result
    raise self._raised
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1030, in run_context
    yield self
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1699, in run_task_sync
    engine.call_task_fn(txn)
    ~~~~~~~~~~~~~~~~~~~^^^^^
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/task_engine.py", line 1047, in call_task_fn
    result = call_with_parameters(self.task.fn, parameters)
  File "/home/ogaudel/Dev/recon_bot/.venv/lib/python3.13/site-packages/prefect/utilities/callables/__init__.py", line 404, in call_with_parameters
    return fn(*args, **kwargs)
  File "/home/ogaudel/Dev/recon_bot/tasks.py", line 48, in port_scan_task
    result = scan_ports_and_takeover(domain, Path(output_dir) if output_dir else None)
  File "/home/ogaudel/Dev/recon_bot/modules/port_scanner.py", line 20, in scan_ports_and_takeover
    raise FileNotFoundError(f"[!] Erreur: {input_file} introuvable. Lance subdomain_recon d'abord.")
FileNotFoundError: [!] Erreur: /home/ogaudel/Dev/recon_bot/outputs/duraline_com/duraline_com_live.txt introuvable. Lance subdomain_recon d'abord.
17:21:56.706 | INFO    | prefect - Stopping temporary server on http://127.0.0.1:8721
