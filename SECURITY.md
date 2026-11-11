# Security Policy

## Reporting a vulnerability

Please do not report security issues in public GitHub issues.

Report them privately through GitHub Security Advisories on this
repository: open the **Security** tab and choose **Report a
vulnerability**. Issues in the chDB engine itself can be reported the
same way on [chdb-io/chdb](https://github.com/chdb-io/chdb/security).

## Scope

This repository ships agent skills and plugin metadata only. It contains
no executable server code; the bundled `verify_install.py` scripts only
import the `chdb` Python package and run sample queries.
