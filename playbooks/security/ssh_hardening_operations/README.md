## SSH hardening operations

- Remove/Enable root login
- Add the local public key to host for root login
- Disable password authentication
- Change the ssh port to 8443 (This requires semanage command to be run on host to add 8443 as a ssh port)


semanage command
```
sudo semanage port -m -t ssh_port_t -p tcp 8443
```
