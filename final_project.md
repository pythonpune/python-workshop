# It's time to solve the riddle

## Tools we need before starting

### Install pip
```
$python3 -m ensurepip
```

### Create a virtualenv and activate it
```
$ python3 -m venv fossmeet
$ source fossmeet/bin/activate
```

### Install requests python module
```
$ python3 -m pip install requests
```

## It's time to follow next steps

Here is the github contributions API url
https://api.github.com/repos/python/cpython/stats/contributors

[1.] Create a github token to access github API by following this
     link: https://github.com/settings/tokens/new

[2.] Copy the token store it safely in a file

[3.] Create a file name github_repo_contributors.py

[4.] Create first function which will ask for your github
     username and token and return it as a tuple.

[5.] Import requests module, then use *requests.get* method to
     call the github API and then store the response
     * check the response status code if it is not 200
        then raise exception with proper message.
     * If you get the response code == 200 then use json module
       and dump response data in contribution.json

[6.] Since we have data now, create another function which will
      return contributors name and their contributions

[7.] Procced with first top 10 contributors name

[8.] Print the no. of contributors with same commit.
