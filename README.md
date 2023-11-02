## integrit

[![CI](https://github.com/Oefenweb/ansible-integrit/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-integrit/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-integrit-blue.svg)](https://galaxy.ansible.com/Oefenweb/integrit)

Set up integrit in Debian-like systems.

#### Requirements

None

#### Variables

* `integrit_configs` [default: `[/etc/integrit/integrit.conf]`]: Configuration file(s)
* `integrit_email_rcpt` [default: `root`]: The mail address reports are sent to
* `integrit_email_subj` [default: ``'[integrit] `hostname -f`: report on changes in the filesystems'``]: The subject line for the report mails
* `integrit_always_email` [default: `false`]: If set to `true`, a report is mailed on every run

* `integrit_root` [default: `'/'`]: The root of the filetree that integrit will cover
* `integrit_known_db` [default: `'/var/lib/integrit/known.cdb'`]: The location of the known database (which contains information about the previous state of the host's files)
* `integrit_current_db` [default: `'/var/lib/integrit/current.cdb'`]: The location of the current database (the one to be generated if integrit is doing an update)

* `integrit_rules` [default: see `defaults/main.yml`]: Rules to specify how to treat various parts of the filesystem, see http://integrit.sourceforge.net/texinfo/integrit.html

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - oefenweb.integrit
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-integrit/issues)!
