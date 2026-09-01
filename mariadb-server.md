# MariaDB Server

MariaDB is a widely-used, open-source relational database management system, developed as a community-driven fork of MySQL by its original creators. It powers production workloads across web infrastructure, enterprise data platforms, and cloud providers (AWS, Google Cloud), and is maintained through a formal contributor/reviewer process by the MariaDB Foundation and Corporation engineering teams.

<a href="https://github.com/MariaDB/server">Github Repo</a>

## My Contributions
* <a href="https://github.com/MariaDB/server/pull/5405">PR 5405</a> | <a href="https://jira.mariadb.org/browse/MDEV-40174">MDEV-40174</a> : Eliminated redundant double-parsing in the `json_normalize`/`json_equals` engine by removing the `json_valid_engine` pre-validation pass and folding its checks into the single `json_norm_build` parse: propagating parse errors (`err || je->s.error`), detecting empty/uninitialized input, and scanning to end-of-document post-parse to catch trailing garbage after valid scalars. Merged into the `10.11` branch.
