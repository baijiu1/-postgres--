# 令人惊叹的 postgresql

PostgreSQL，通常只是Postgres，是一个对象关系数据库（ORDBMS）。PostgreSQL是符合ACID和事务性的。（见更多：维基百科：PostgreSQL，PostgreSQL.org）



## 内容

- 令人惊叹的 postgresql
    - [高可用性](#high-availability)
    - [备份](#backups)
    - [GUI](#gui)
    - [分布](#distributions)
    - [CLI](#cli)
    - [服务](#server)
    - [监控](#monitoring)
    - [扩展](#extensions)
    - [优化](#optimization)
    - [公共事业](#utilities)
    - [语言绑定](#language-bindings)
    - [PaaS (PostgreSQL as a Service)](#paas-postgresql-as-a-service)
    - [Docker images](#docker-images)
- [资源](#resources)
    - [教程](#tutorials)
    - [博客](#blogs)
    - [文章](#articles)
    - [文档](#documentation)
    - [新闻](#newsletters)
    - [视频](#videos)
    - [社区](#community)

### 高可用性
* [BDR](https://github.com/2ndQuadrant/bdr) - 双向复制 - PostgreSQL的多主机复制系统
* [Patroni](https://github.com/zalando/patroni) - 带有ZooKeeper或etcd的PostgreSQL HA模板。
* [Stolon](https://github.com/sorintlab/stolon) - PostgreSQL HA基于Consul或etcd，与Kubernetes集成。
* [pglookout](https://github.com/aiven/pglookout) - 复制监视和故障转移守护程序。
* [repmgr](https://github.com/2ndQuadrant/repmgr) - 用于管理PostgreSQL服务器集群中的复制和故障转移的开源工具套件。
* [Slony-I](http://slony.info) - 具有级联和故障转移功能的“Master to multiple slaves”复制系统。
* [PAF](https://github.com/ClusterLabs/PAF) - PostgreSQL自动故障转移：Postgres的高可用性，基于Pacemaker和Corosync。
* [SkyTools](https://github.com/pgq/skytools-legacy) - 复制工具，包括排队系统PgQ和Londiste，这是一个比Slony管理起来更简单的复制系统。

### Backups
* [Barman](https://www.pgbarman.org/index.html) - 2ndQuadrant的PostgreSQL备份和恢复管理器。
* [OmniPITR](https://github.com/omniti-labs/omnipitr) - PostgreSQL的高级WAL文件管理工具。
* [pg\_probackup](https://github.com/postgrespro/pg_probackup) – 由@PostgresPro改进的pg_arman的分支，支持增量备份，从副本备份，多线程备份和还原，以及无归档命令的匿名备份。
* [pgBackRest](https://pgbackrest.org/)  - 可靠的PostgreSQL备份和恢复。
* [pg\_back](https://github.com/orgrim/pg_back/) - pg_back是一个简单的备份脚本
* [pghoard](https://github.com/aiven/pghoard) - 云对象存储的备份和恢复工具（AWS S3，Azure，Google Cloud，OpenStack Swift）。
* [wal-e](https://github.com/wal-e/wal-e) - Heroku将PostgreSQL简单连续存档到S3，Azure或Swift。
* [wal-g](https://github.com/wal-g/wal-g) - 在Go中重写的WAL-E的继承者。目前仅支持S3。
* [pitrery](https://dalibo.github.io/pitrery/) - pitrery是一组用于管理PostgreSQL的即时恢复（PITR）备份的Bash脚本。

### GUI
* [Adminer](https://www.adminer.org/) - 用PHP编写的全功能数据库管理工具。
* [OmniDB](https://omnidb.org/en/) - 数据库管理的开源协作环境
* [DataGrip](https://www.jetbrains.com/datagrip/) - 具有高级工具集和良好的跨平台经验的IDE（商业软件）。
* [Datazenit](https://datazenit.com/) - 基于Web的PostgreSQL GUI（商业软件）。
* [DBeaver](https://dbeaver.io/) - 通用数据库管理器，对PostgreSQL提供出色的支持。
* [dbglass](http://dbglass.web-pal.com) - PostgreSQL的跨平台桌面客户端，使用Electron构建。
* [Holistics](https://www.holistics.io/) - 具有强大PostgreSQL支持的在线跨平台数据库管理工具和SQL查询报告GUI（商业软件）。
* [JackDB](https://www.jackdb.com/) - 基于Web的SQL查询界面（商业软件）。
* [Metabase](https://www.metabase.com/) - PostgreSQL的简单仪表板，图表和查询工具。
* [Numeracy](https://numeracy.co/) - 带有PostgreSQL（商业软件）图表和仪表板的快速SQL编辑器。
* [pgAdmin](https://www.pgadmin.org/) - PostgreSQL管理和管理GUI。
* [pgModeler](https://pgmodeler.io/) - pgModeler是一个开源的PostgreSQL数据库建模器。
* [pgweb](https://github.com/sosedoff/pgweb) - 用Go编写的基于Web的PostgreSQL数据库浏览器。
* [phpPgAdmin](https://github.com/phppgadmin/phppgadmin) - PostgreSQL的Premier Web管理工具。
* [Postbird](https://github.com/Paxa/postbird) - 用于macOS的PostgreSQL客户端。
* [Postico](https://eggerapps.at/postico/) - 用于macOS的现代PostgreSQL客户端（商业软件）。
* [PSequel](http://www.psequel.com/) - 简洁的界面，可快速执行常见的PostgreSQL任务（商业软件）。
* [SQL Tabs](http://www.sqltabs.com/) - 用JS编写的PostgreSQL跨平台桌面客户端。
* [SQLPro for Postgres](http://macpostgresclient.com/) - 用于macOS（商业软件）的简单，强大的PostgreSQL管理器。
* [temBoard](https://github.com/dalibo/temboard) - 基于Web的PostgreSQL GUI和监控。
* [TablePlus](https://tableplus.io/) - 允许您编辑数据库和结构的Native App。确保高端安全性（商业软件）。
* [TeamSQL](https://teamsql.io/) - 跨平台SQL客户端：简单，轻松，可扩展。
* [Valentina Studio](https://www.valentina-db.com/en/valentina-studio-overview) - 跨平台数据库管理工具（免费/商业）
* [PostgresCompare](https://www.postgrescompare.com) - 跨平台数据库比较和部署工具（商业软件）。

### 分布
* [Postgres.app](https://postgresapp.com/) - 在macOS上开始使用PostgreSQL的最简单方法。
* [PostgreSql.Binaries.Lite](https://github.com/mihasic/PostgreSql.Binaries.Lite) - PostgreSQL数据库的最小Windows二进制文件集。也通过NuGet提供。

### CLI
* [pgcli](https://github.com/dbcli/pgcli) - Postgres CLI具有自动完成和语法突出显示功能
* [psql](https://www.postgresql.org/docs/current/static/app-psql.html) - 内置的PostgreSQL CLI客户端
* [psql2csv](https://github.com/fphilipe/psql2csv) - 在psql中运行查询并将结果输出为CSV

### Server
* [Postgres-XL](https://www.postgres-xl.org/) - 基于PostgreSQL的可扩展开源数据库集群。
* [AgensGraph](https://bitnine.net/) - 基于PostgreSQL的强大图形数据库。
* [Greenplum Database](https://github.com/greenplum-db/gpdb) - 用于大数据量的PostgreSQL的开源分支。

### 监控
* [check\_pgactivity](https://github.com/OPMDG/check_pgactivity) - check_pgactivity旨在监控Nagios中的PostgreSQL集群。它提供了许多选项来衡量和监控有用的性能指标。
* [Check\_postgres](https://github.com/bucardo/check_postgres) - 用于检查PostgreSQL数据库状态的Nagios check_postgres插件。
* [Instrumental](https://github.com/Instrumental/instrumentald) - 实时性能监控，包括易于设置的[pre-made graphs](https://instrumentalapp.com/docs/instrumentald/postgresql#suggested-graphs) （商业软件） 
* [libzbxpgsql](https://github.com/cavaliercoder/libzbxpgsql) - Zabbix的综合PostgreSQL监控模块。
* [Pome](https://github.com/rach/pome) - Pome代表PostgreSQL指标。Pome是一个PostgreSQL指标仪表板，用于跟踪数据库的运行状况。
* [pg\_view](https://github.com/zalando/pg_view) - 开源命令行工具，显示全局系统统计信息，每个分区信息，内存统计信息和其他信息。
* [pgwatch2](https://github.com/cybertec-postgresql/pgwatch2) - 灵活且易于上手的PostgreSQL指标监控重点关注Grafana仪表板。
* [pgbench](https://www.postgresql.org/docs/devel/static/pgbench.html) - 在PostgreSQL上运行基准测试。
* [opm.io](http://opm.io) -  Open PostgreSQL Monitoring是一个免费软件套件，旨在帮助您管理PostgreSQL服务器。它可以收集统计信息，显示仪表板并在出现问题时发送警告。
### 扩展
* [Citus](https://github.com/citusdata/citus) - 可扩展的PostgreSQL集群，用于实时工作负载。
* [cstore\_fdw](https://github.com/citusdata/cstore_fdw) - 使用PostgreSQL进行分析的列式存储。
* [cyanaudit](https://pgxn.org/dist/cyanaudit/) - Cyan Audit以逐列为基础提供所有DML活动的数据库内日志记录。
* [pglogical](https://github.com/2ndQuadrant/pglogical) - 提供逻辑流复制的扩展。
* [pg\_partman](https://github.com/pgpartman/pg_partman) - PostgreSQL的分区管理扩展。
* [pg\_paxos](https://github.com/citusdata/pg_paxos/) - PostgreSQL节点集群的Paxos和基于Paxos的表复制的基本实现。
* [pg\_shard](https://github.com/citusdata/pg_shard) - 扩展以扩展实时读写。
* [PGStrom](https://wiki.postgresql.org/wiki/PGStrom) - 将CPU密集型工作负载卸载到GPU的扩展。
* [pgxn](https://pgxn.org/) PostgreSQL Extension Network - PostgreSQL扩展网络 - 许多开源PostgreSQL扩展的中心分发点
* [PipelineDB](https://www.pipelinedb.com/) - PostgreSQL扩展，在流上连续运行SQL查询，逐步将结果存储在表中。
* [plpgsql\_check](https://github.com/okbob/plpgsql_check) - 允许检查plpgsql源代码的扩展。
* [PostGIS](http://postgis.net/) - PostgreSQL的空间和地理对象。
* [PG\_Themis](https://github.com/cossacklabs/pg_themis) - Postgres绑定作为加密库Themis的扩展，在PgSQL方面提供各种安全服务。
* [zomboDB](https://github.com/zombodb/zombodb) - 通过使用Elasticsearch支持的索引实现高效全文搜索的扩展。
* [pgMemento](https://github.com/pgMemento/pgMemento) - 使用PL / pgSQL编写的触发器和服务器端函数为PostgreSQL数据库内的数据提供审计跟踪。
* [Timescale](https://www.timescale.com/) - 与Postgres完全兼容的开源时间序列数据库，作为扩展分发
* [pgTAP](https://pgtap.org/) - Postgres的数据库测试框架
* [HypoPG](https://github.com/HypoPG/hypopg) - HypoPG提供假设/虚拟索引功能。
* [pgRouting](https://github.com/pgRouting/pgrouting) - pgRouting扩展了PostGIS / PostgreSQL地理空间数据库，以提供地理空间路由和其他网络分析功能。

### 优化
* [PgHero](https://github.com/ankane/pghero) - PostgreSQL insights made easy.
* [pgtune](https://github.com/gregs1104/pgtune/) - PostgreSQL configuration wizard.
* [pgtune](https://github.com/le0pard/pgtune) - Online version of PostgreSQL configuration wizard.
* [pgconfig.org](https://github.com/sebastianwebber/pgconfig) - PostgreSQL Online Configuration Tool (also based on pgtune).
* [PoWA](https://powa.readthedocs.io/en/latest/) - PostgreSQL Workload Analyzer gathers performance stats and provides real-time charts and graphs to help monitor and tune your PostgreSQL servers.
* [pg_web_stats](https://github.com/kirs/pg_web_stats) - Web UI to view pg_stat_statements.

### Utilities
* [apgdiff](https://www.apgdiff.com/) - Compares two database dump files and creates output with DDL statements that can be used to update old database schema to new one.
* [ERAlchemy](https://github.com/Alexis-benoist/eralchemy) - ERAlchemy generates Entity Relation (ER) diagram from databases.
* [ldap2pg](https://github.com/dalibo/ldap2pg) - Synchronize roles and privileges from YML and LDAP.
* [mysql-postgresql-converter](https://github.com/lanyrd/mysql-postgresql-converter) - Lanyrd's MySQL to PostgreSQL conversion script.
* [ora2pg](http://ora2pg.darold.net) - Perl module to export an Oracle database schema to a PostgreSQL compatible schema.
* [pg\_activity](https://github.com/julmon/pg_activity) - top like application for PostgreSQL server activity monitoring.
* [pg-formatter](https://github.com/gajus/pg-formatter) - A PostgreSQL SQL syntax beautifier (Node.js).
* [pganalyze](https://pganalyze.com) - PostgreSQL Performance Monitoring (Commercial Software).
* [pgbadger](https://github.com/darold/pgbadger) - Fast PostgreSQL Log Analyzer.
* [PgBouncer](http://pgbouncer.github.io) - Lightweight connection pooler for PostgreSQL.
* [pgCenter](https://github.com/lesovsky/pgcenter) - Provides convenient interface to various statistics, management task, reloading services, viewing log files and canceling or terminating database backends.
* [pg_chameleon](https://github.com/the4thdoctor/pg_chameleon) - Real time replica from MySQL to PostgreSQL with optional type override migration and migration capabilities.
* [pgclimb](https://github.com/lukasmartinelli/pgclimb) - Export data from PostgreSQL into different data formats.
* [pgfutter](https://github.com/lukasmartinelli/pgfutter) - Import CSV and JSON into PostgreSQL the easy way.
* [PGInsight](http://pginsight.io/) - CLI tool to easily dig deep inside your PostgreSQL database.
* [pgloader](https://github.com/dimitri/pgloader) - Loads data into PostgreSQL using the COPY streaming protocol, and does so with separate threads for reading and writing data.
* [pgMustard](https://www.pgmustard.com/) - A modern user interface
for `EXPLAIN ANALYSE`, that also provides performance tips (Commercial Software).
* [pgpool-II](http://www.pgpool.net/mediawiki/index.php/Main_Page) - Middleware that provides connection pooling, replication, load balancing and limiting exceeding connections.
* [pgsync](https://github.com/ankane/pgsync) - Tool to sync PostgreSQL data to your local machine.
* [PGXN client](https://github.com/pgxn/pgxnclient) - Command line tool to interact with the PostgreSQL Extension Network
* [postgresql-metrics](https://github.com/spotify/postgresql-metrics) - Tool that extracts and provides metrics for your PostgreSQL database.
* [PostgREST](https://github.com/PostgREST/postgrest) - Serves a fully RESTful API from any existing PostgreSQL database.
* [pREST](https://github.com/prest/prest) - Serve a RESTful API from any PostgreSQL database (Golang)
* [PostGraphile](https://github.com/graphile/postgraphile) - Instant GraphQL API or GraphQL schema for your PostgreSQL database
* [yoke](https://github.com/nanopack/yoke) - PostgreSQL high-availability cluster with auto-failover and automated cluster recovery.
* [pglistend](https://github.com/kabirbaidhya/pglistend) - A lightweight PostgresSQL `LISTEN`/`NOTIFY` daemon built on top of `node-postgres`.
* [ZSON](https://github.com/postgrespro/zson) - PostgreSQL extension for transparent JSONB compression
* [pg_bulkload](http://ossc-db.github.io/pg_bulkload/index.html) - It's a high speed data loading utility for PostgreSQL.
* [pg_migrate](https://github.com/jwdeitch/pg_migrate) - Manage PostgreSQL codebases and make VCS simple.
* [sqitch](https://github.com/sqitchers/sqitch) - Tool for managing versioned schema deployment
* [pgmigrate](https://github.com/yandex/pgmigrate) - CLI tool to evolve schema migrations, developed by Yandex.
* [pgcmp](https://github.com/cbbrowne/pgcmp) - Tool to compare database schemas, with capability to accept some persistent differences
* [graphql-engine](https://github.com/hasura/graphql-engine) - Get Instant Realtime GraphQL APIs over PostgreSQL.
* [sqlcheck](https://github.com/jarulraj/sqlcheck) - Automatically detects common SQL anti-patterns. Such anti-patterns often slow down queries. Addressing them will, therefore, help accelerate queries.

### Language bindings
* Common Lisp: [Postmodern](https://github.com/marijnh/Postmodern)
* Clojure: [clj-postgresql](https://github.com/remodoy/clj-postgresql)
* Elixir: [postgrex](https://github.com/elixir-ecto/postgrex)
* Go: [pgx](https://github.com/jackc/pgx)
* Haskell: [postgresql-simple](http://hackage.haskell.org/package/postgresql-simple)
* Java: [PostgreSQL JDBC Driver](https://jdbc.postgresql.org/)
* .Net/.Net Core: [Npgsql](https://github.com/npgsql/npgsql)
* Node: [node-postgres](https://github.com/brianc/node-postgres), [pg-promise](https://github.com/vitaly-t/pg-promise), [pogi](https://github.com/holdfenytolvaj/pogi)
* Perl: [DBD-Pg](https://metacpan.org/pod/distribution/DBD-Pg/Pg.pm)
* PHP: [Pomm](http://www.pomm-project.org), [pecl/pq](https://github.com/m6w6/ext-pq)
* Python: [psycopg2](https://pypi.org/project/psycopg2/)
* Ruby: [pg](https://bitbucket.org/ged/ruby-pg/wiki/Home)
* Rust: [rust-postgresql](https://github.com/sfackler/rust-postgres)
* Lua: [luapgsql](https://github.com/arcapos/luapgsql)

### PaaS *(PostgreSQL as a Service)*
* [Aiven PostgreSQL](https://aiven.io/postgresql) - PostgreSQL as a service in AWS, Azure, DigitalOcean, Google Cloud and UpCloud; plans range from $19/month single node instances to large highly-available setups, free trial for two weeks.
* [Amazon RDS for PostgreSQL](https://aws.amazon.com/rds/postgresql/) - Amazon Relational Database Service (RDS) for PostgreSQL
* [Azure Database for PostgreSQL](https://azure.microsoft.com/en-us/services/postgresql/) - Azure Database for PostgreSQL provides fully managed, enterprise-ready community PostgreSQL database as a service. It provides builtin HA, elastic scaling and native integration with Azure ecosystem.
* [Citus Cloud](https://www.citusdata.com/product/cloud) - Production grade scaled out PostgreSQL as a service enabling real-time workloads and sharding your multi-tenant apps.
* [Compose](https://www.compose.com/databases/postgresql) - PostgreSQL as a service in AWS, Google Cloud Platform, and IBM Cloud; plans range from $17.5/month for 1GB storage and scale at $12/GB beyond that. Free trial for 30 days available.
* [Database Labs](https://www.databaselabs.io) - Get a production-ready cloud PostgreSQL server in minutes, from $20 a month Backups, monitoring, patches, and 24/7 tech support all included.
* [DigitalOcean Managed Databases](https://www.digitalocean.com/products/managed-databases/) - Fully managed PostgreSQL databases. No free plan. Starting at $15/mo. Daily backups with point-in-time recovery. Standby nodes with auto-failover.
* [ElephantSQL](https://www.elephantsql.com/) - Offers databases ranging from shared servers for smaller projects and proof of concepts, up to enterprise grade multi server setups. Has free plan for up to 5 DBs, 20 MB each.
* [Google Cloud SQL for PostgreSQL](https://cloud.google.com/sql/docs/postgres/) - Fully-managed database service that makes it easy to set up, maintain, manage, and administer your PostgreSQL relational databases on Google Cloud Platform. (Beta)
* [Heroku Postgres](https://elements.heroku.com/addons/heroku-postgresql) - Plans from free to huge, operated by PostgreSQL experts. Does not require running your app on Heroku. Free plan includes 10,000 rows, 20 connections, up to two backups, and has PostGIS support.

### Docker images
* [citusdata/citus](https://hub.docker.com/r/citusdata/citus/) - Citus official images with citus extensions. Based on the official Postgres container.
* [mdillon/postgis](https://hub.docker.com/r/mdillon/postgis/) - PostGIS 2.3 on Postgres 9. Based on the official Postgres container.
* [postgres](https://hub.docker.com/_/postgres/) -  Official postgres container (from Docker)

## Resources

### Tutorials
* [Backup and recover a PostgreSQL DB using wal-e](https://coderwall.com/p/cwe2_a/backup-and-recover-a-postgres-db-using-wal-e) - Tutorial about setting up continuous archiving in PostgreSQL using wal-e.
* [PG Casts](https://www.pgcasts.com) - Free weekly PostgreSQL screencasts by Hashrocket.
* [Postgres Guide](http://postgresguide.com/) - Guide designed as an aid for beginners and experienced users to find specific tips and explore tools available within PostgreSQL.
* [PostgreSQL Exercises](https://pgexercises.com/) - Site  to make it easy to learn PostgreSQL by doing exercises.
* [tutorialspoint PostgreSQL tutorial](http://www.tutorialspoint.com/postgresql/) - Very extensive collection of tutorials on PostgreSQL
* [postgresDBSamples](https://github.com/morenoh149/postgresDBSamples) - A collection of sample postgres schemas
* [PostgreSQL Primer for Busy People](https://zaiste.net/postgresql_primer_for_busy_people/) - A collection of the most common commands used in PostgreSQL
* [pg-utils](https://github.com/dataegret/pg-utils) - Useful DBA tools by Data Egret

### Blogs
* [Planet PostgreSQL](https://planet.postgresql.org/) - Blog aggregation service for PostgreSQL.
* [Andrew Dunstan's PostgreSQL and Technical blog](http://adpgtech.blogspot.com/search/label/PostgreSQL/)
* [Bruce Momjian's PostgreSQL blog](http://momjian.us/main/blogs/pgblog.html)
* [Craig Kerstiens PostgreSQL posts](http://www.craigkerstiens.com/categories/postgres/) - Set of posts on PostgreSQL cool features, tips and tricks.
* [Database Soup](http://www.databasesoup.com/search/label/postgresql/) - Josh Berkus' blog.
* [Michael Paquier's blog](https://paquier.xyz/)
* [Robert Haas' blog](http://rhaas.blogspot.com/search/label/postgresql/)
* [select * from depesz;](https://www.depesz.com/tag/postgresql/) - Hubert Lubaczewski's blog.

### Articles

* [What PostgreSQL has over other open source SQL databases: Part I](https://www.compose.com/articles/what-postgresql-has-over-other-open-source-sql-databases/)
* [Debugging PostgreSQL performance, the hard way](https://www.justwatch.com/blog/post/debugging-postgresql-performance-the-hard-way/)
* [Why use Postgres?](http://www.craigkerstiens.com/2017/04/30/why-postgres-five-years-later/)
* [Superfast CSV imports using PostgreSQL's COPY command](https://infinum.co/the-capsized-eight/superfast-csv-imports-using-postgresqls-copy)

### Documentation
* [Wiki](https://wiki.postgresql.org/wiki/Main_Page) - user documentation, how-tos, and tips 'n' tricks

### Newsletters

* [Postgres Weekly](https://postgresweekly.com/) - Weekly newsletter that contains articles, news, and repos relevant to PostgreSQL.

### Videos
* [Citus Data Youtube channel](https://www.youtube.com/channel/UC8jpoK1BqQhDh6HDGFnM_DA/videos) - Citus related videos
* [EnterpriseDB Youtube channel](https://www.youtube.com/channel/UCkIPoYyNr1OHgTo0KwE9HJw) -  EnterpriseDB related videos
* [PGConf US Youtube channel](https://www.youtube.com/pgconfus/) - Conference videos

### Community
* [Mailing lists](https://www.postgresql.org/list/) - Official mailing lists for Postgres for support, outreach, and more. One of the primary channels of communication in the Postgres community. 
* [Slack](https://postgres-slack.herokuapp.com/) - Slack channel for Postgres with close to 5000 users
* [#postgresql on Freenode](https://webchat.freenode.net/?channels=postgresql) - The most popular IRC channel about Postgres on Freenode with close to 1000 users 
* [Reddit](https://www.reddit.com/r/PostgreSQL/) - A reddit community for PostgreSQL users with close to 10000 users
