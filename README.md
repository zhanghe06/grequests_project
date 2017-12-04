## GRequests Test Project


### GRequests: Asynchronous Requests

https://github.com/kennethreitz/grequests

### create python2 virtual environment
```
virtualenv -p /usr/local/bin/python2 grequests.py2.env
source grequests.py2.env/bin/activate
pip install grequests
pip install -r requirements.py2.txt
```

### create python3 virtual environment
```
virtualenv -p /usr/local/bin/python3 grequests.py3.env
source grequests.py3.env/bin/activate
pip install grequests
pip install -r requirements.py3.txt
```


### test reports

- test environment:
Mac Pro macOS High Sierra
- test contents:
http://www.baidu.com domain 200 concurrent requests

```
# python2 environment
(grequests.py2.env) ➜  grequests_project python tests/get_baidu_requests.py
6.46457982063
(grequests.py2.env) ➜  grequests_project python tests/get_baidu_grequests.py
0.7383248806

# python3 environment
(grequests.py3.env) ➜  grequests_project python tests/get_baidu_requests.py
5.181720018386841
(grequests.py3.env) ➜  grequests_project python tests/get_baidu_grequests.py
0.8184318542480469
```

- test environment:
Mac Pro macOS High Sierra
- test contents:
https://www.baidu.com domain 200 concurrent requests
```
# python2 environment
(grequests.py2.env) ➜  grequests_project python tests/get_baidu_requests.py
12.3944959641
(grequests.py2.env) ➜  grequests_project python tests/get_baidu_grequests.py
2.24422097206

# python3 environment
(grequests.py3.env) ➜  grequests_project python tests/get_baidu_requests.py
12.188169956207275
(grequests.py3.env) ➜  grequests_project python tests/get_baidu_grequests.py
2.3108882904052734
```


The efficiency of `grequests` is an order of magnitude higher than `requests`

HTTPS's request is twice as slow as HTTP
