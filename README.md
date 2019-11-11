Thoth: PostgreSQL Metrics-exporter
==================================

This role will deploy PostgreSQL Metrics exporter for Thoth's knowledge database into an OpenShift namespace.

Role Variables
--------------

This role requires a namespace in which the metrics exporter should be created together with few parameters for PostgreSQL instance. See the ``vars`` configuration section for more info.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters):

    - hosts: localhost
      connection: local
      gather_facts: False

      roles:
        - role: thoth-station.postgresql-metrics-exporter
          namespace: thoth-test-core

Variables of the playbook
-------------------------

The playbook accepts the following variables:


* `namespace` - OpenShift project where the PostgreSQL application should be deployed to (defaults to `thoth-test-core`)
* `postgresql_user` - database user which will be created for accessing database content (defaults to `thoth`)
* `postgresql_password` - password which will be used for the database user (defaults to `thoth`)
* `postgresql_database` - name of the PostgreSQL database (defaults to `postgres`)


License
-------

GPLv3

Author Information
------------------

The Thoth Station Team.