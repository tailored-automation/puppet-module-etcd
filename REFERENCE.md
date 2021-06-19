# Reference
<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

**Classes**

* [`etcd`](#etcd): Manage etcd

## Classes

### etcd

Manage etcd

#### Examples

##### 

```puppet
include etcd
```

#### Parameters

The following parameters are available in the `etcd` class.

##### `version`

Data type: `String`

Version of etcd to install
Not used if download_url is defined.

Default value: '3.4.7'

##### `base_url`

Data type: `Stdlib::HTTPUrl`

Base URL of where to download etcd binaries.
Not used if download_url is defined.

Default value: 'https://github.com/etcd-io/etcd/releases/download'

##### `os`

Data type: `String[1]`

The GOOS to install
Not used if download_url is defined.

Default value: downcase($facts['kernel'])

##### `arch`

Data type: `String[1]`

The GOARCH to install
Not used if download_url is defined.

Default value: $facts['os']['architecture']

##### `download_url`

Data type: `Optional[Stdlib::HTTPUrl]`

Alternative location to download etcd binaries

Default value: `undef`

##### `download_dir`

Data type: `Stdlib::Absolutepath`

The directory of where to download etcd

Default value: '/tmp'

##### `extract_dir`

Data type: `Stdlib::Absolutepath`

The directory where to extract etcd

Default value: '/opt'

##### `bin_dir`

Data type: `Stdlib::Absolutepath`

The path to bin directory for etcd and etcdctl symlinks

Default value: '/usr/bin'

##### `manage_user`

Data type: `Boolean`

Boolean that determines if etcd user is managed

Default value: `true`

##### `manage_group`

Data type: `Boolean`

Boolean that determines if etcd group is managed

Default value: `true`

##### `user`

Data type: `String[1]`

The etcd user

Default value: 'etcd'

##### `user_uid`

Data type: `Optional[Integer]`

The etcd user UID

Default value: `undef`

##### `group`

Data type: `String[1]`

The etcd group

Default value: 'etcd'

##### `group_gid`

Data type: `Optional[Integer]`

The etcd group GID

Default value: `undef`

##### `config_path`

Data type: `Stdlib::Absolutepath`

The path to etcd YAML configuration

Default value: '/etc/etcd.yaml'

##### `config`

Data type: `Hash`

The config values to pass to etcd

Default value: {'data-dir' => '/var/lib/etcd'}

##### `max_open_files`

Data type: `Integer`

The value for systemd LimitNOFILE unit option

Default value: 40000
