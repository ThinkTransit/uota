# Web server for testing

Run `docker compose up -d` to start nginx in Docker and point your `uota.cfg` at your `IP:8080`. `latest` and `test.tgz` are provided but feel free to override them with your own.

## Basic authentication

- username: `test_user`
- password: `t3st_pa$$`

## Certificate for testing of cert. pinning

Not implemented yet.

## Snippets for quick testing

```python
import urequests
auth = None
auth = ('test_user', 't3st_pa$$')
url='http://192.168.1.20:8080/'
response = urequests.get(url + 'latest', auth=auth)
```
