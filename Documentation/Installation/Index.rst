.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../Includes.txt
.. include:: Images.txt

.. _installation:

Installation
============

Upgrade
============
Migrate records from tx_a21glossary_main to tx_a21glossary_domain_model_entry

```sql
INSERT INTO tx_a21glossary_domain_model_entry (
    uid, pid, short, shortcut, longversion, shorttype, language,
    description, link, exclude, force_linking, force_case, force_preservecase,
    force_regexp, force_global
)
SELECT uid, pid, short, shortcut, longversion, shorttype, language,
    description, link, exclude, force_linking, force_case, force_preservecase,
    force_regexp, force_global
FROM tx_a21glossary_main;
```
