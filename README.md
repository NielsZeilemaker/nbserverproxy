# nbserverproxy
Jupyter notebook server extension to proxy web services. This enables users to reach arbitrary web services running within their spawned Jupyter server and is probably most appropriate for services which can't readily be converted into extensions.

## Example
A user starts a web service via `New > Terminal`:
```
echo "hello world" > index.html
python -m http.server 8001
```
The service is proxied off of `/proxy/` at https://address.of.notebook.server/user/theuser/proxy/8001.

## Installation
Install via Conda:
```
conda install -c conda-forge nbserverproxy
```

or 

Install from git repo:

```
pip install git+https://github.com/jupyterhub/nbserverproxy
jupyter serverextension enable --py nbserverproxy
```

Based on https://github.com/senko/tornado-proxy.
