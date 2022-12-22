# About
This batch script will help you install and run the 9Hits application without GUI to start earning points, any patchs are welcome :)
![9Hits App](https://raw.githubusercontent.com/9hitste/install/main/9happv3.png))
# Requirements
Works best on Ubuntu 18, and Debian 10. The other distros should work but are not well tested.
# Install
curl -sSLk https://raw.githubusercontent.com/OwElko/9Hitsinstall/main/linux.sh | sudo bash -s -- options
# Available options
| Option | Description |
| --- | --- |
| --install-dir | Where to download and extract the 9Hits App, default is $HOME |
| --mode | `exchange`, `bot` or `profile` (default is `exchange`) |
| --token | Your [9Hits token](https://panel.9hits.com/user/profile) |
| --note | Note for the computer that install the 9Hits App, useful on the remote page |
| --allow-popups | `yes` or `no` |
| --allow-adult | `yes` or `no` |
| --allow-crypto | `yes` or `no` |
| --system-session | Create the system session (that use the real IP of the machine) |
| --ex-proxy-sessions | Number of the sessions that use external proxy |
| --ex-proxy-url | The proxy pool url, leave empty to use 9hits proxy (not recommended) |
| --session-note | Note for the created sessions |
| --ssh-connector | `putty` or `ssh2` (`putty` is recommended) |
| --cache-dir | Override the default cache dir |
| --create-swap | Create swap, eg: --create-swap=10G |
| --cache-del | `0`: no cache, `-1`: never delete cache, `100-200-500-1000`: clear cache after corresponding number of views |
| --auto-start | Auto start on startup |
| --hide-browser | Hide browser |
| --clear-all-sessions | Clear all created session (if exists from previous install) |
| --no-cronjob | Does not create cronjob to start the viewer |
# Examples
- Run 1 system session:
```
curl -sSLk https://raw.githubusercontent.com/OwElko/9Hitsinstall/main/linux.sh | sudo bash -s -- --token=186eaced825ab3e3468dfda97d880123 --system-session --allow-crypto=no
```
- Run 1 system session + 10 session use 9hits pool:
```
curl -sSLk https://raw.githubusercontent.com/OwElko/9Hitsinstall/main/linux.sh | sudo bash -s -- --token=186eaced825ab3e3468dfda97d880123 --system-session --ex-proxy-sessions=10 --allow-crypto=no --session-note=9hits-pool --note=my-laptop --hide-browser

```
- Run 1 system session + 10 session use your own pool
```
curl -sSLk https://raw.githubusercontent.com/OwElko/9Hitsinstall/main/linux.sh | sudo bash -s -- --token=186eaced825ab3e3468dfda97d880123 --system-session --ex-proxy-sessions=10 --ex-proxy-url=http://my_pool_url/ --allow-crypto=no --session-note=http-pool --note=my-vps --hide-browser
```
