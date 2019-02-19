# satellite_storage - configures storage for Satellite Server or Satellite Capsule

## Synopsis
An Ansible role for configuring logical volumes and mount points for Satellite Server(s)

See [Satellite 6 Installation Guide - 1.2.1 Storage Requirments](https://access.redhat.com/documentation/en-us/red_hat_satellite/6.4/html/installing_satellite_server_from_a_connected_network/preparing_your_environment_for_installation#storage_requirements) for details on sizing.

## Options

| parameter                        | required | default       | choices | comments                                              |
|----------------------------------|----------|---------------|---------|-------------------------------------------------------|
| satellite\_pvs                   | yes      | /dev/vdb      |         | Physical volume(s) to use for Satellite storage.      |
| satellite\_vg                    | yes      | satellite\_vg |         | Volume group to use or create for Satellite storage.  |
| satellite\_lv\_pulp\_size        | yes      | 10g           |         | Initial size of the `/var/lib/pulp` volume.           |
| satellite\_lv\_pulp\_cache\_size | yes      | 5g            |         | Initial size of the `/var/cache/pulp` volume.         |
| satellite\_lv\_mongodb\_size     | yes      | 0g            |         | Initial size of the `/var/lib/mongodb` volume.        |
| satellite\_lv\_pgsql\_size       | yes      | 0g            |         | Initial size of the `/var/lib/pgsql` volume.          |
