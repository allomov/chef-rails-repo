### build-essential
[link](https://github.com/hw-cookbooks/build-essential)
Installs packages required for compiling C software from source. Use this cookbook if you wish to compile C programs, or install RubyGems with native extensions.



### postgresql
[link](https://github.com/hw-cookbooks/postgresql)
Installs and configures PostgreSQL as a client or a server.
Attributes: 
- node['postgresql']['version'] - version of postgresql to manage
- node['postgresql']['dir'] - home directory of where postgresql data and configuration lives.

- node['postgresql']['client']['packages'] - An array of package names that should be installed on "client" systems.

- node['postgresql']['server']['packages'] - An array of package names that should be installed on "server" systems.
- node['postgresql']['server']['config_change_notify'] - Type of notification triggered when a config file changes.
- node['postgresql']['contrib']['packages'] - An array of package names that could be installed on "server" systems for useful sysadmin tools.

- node['postgresql']['enable_pgdg_apt'] - Whether to enable the apt repo by the PostgreSQL Global Development Group, which contains newer versions of PostgreSQL.

- node['postgresql']['enable_pgdg_yum'] - Whether to enable the yum repo by the PostgreSQL Global Development Group, which contains newer versions of PostgreSQL.

- node['postgresql']['initdb_locale'] - Sets the default locale for the database cluster. 

The following attributes are generated in recipe[postgresql::server].

node['postgresql']['password']['postgres'] - randomly generated password by the openssl cookbook's library. (TODO: This is broken, as it disables the password.)


### rvm
[link](https://github.com/fnichol/chef-rvm)
node['rvm']['rubies'] 
