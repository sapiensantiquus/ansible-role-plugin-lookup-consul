# ansible-role-plugin-lookup-consul

A plugin to look up values by key in Consul, allowing a custom host and port.

Make sure to point your lookup plugins in ansible.cfg to the <strong>role_name</strong>/plugins/lookup

Ex:
```
lookup_plugins = ./roles/consul_lookup/plugins/lookup
```

The lookup can be done as per convention, but with the added url parameter:
```
{{ lookup('consul_lookup', 'key_to_lookup url=http://somehost:8500') }}
```

