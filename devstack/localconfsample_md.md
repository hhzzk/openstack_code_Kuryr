# local.conf.sample

devstack 的样例配置文件。

```sh
[[local|localrc]]

LOGFILE=stack.sh.log
LOG_COLOR=False

DATABASE_PASSWORD=pass
RABBIT_PASSWORD=pass
SERVICE_PASSWORD=pass
SERVICE_TOKEN=pass
ADMIN_PASSWORD=pass

enable_plugin kuryr http://git.openstack.org/openstack/kuryr
enable_service kuryr
enable_service etcd-server
enable_service docker-engine

# Use Neutron instead of nova-network
disable_service n-net
enable_service q-svc
enable_service q-dhcp
enable_service q-l3
disable_service heat
enable_service q-agt
disable_service tempest
```
