hubot-gitlab
============

Hubot Script for providing webhooks for Gitlab

# Installation

For this script to take effect first install it with:

```
npm install --save hubot-gitlab-hooks
```

For this script to track your system events put this URL in as system hook:

```
http://<HUBOT_URL>/gitlab/system
```

For each Repository which should be tracked through the system use this URL as your web hook:

```
Put http://<HUBOT_URL>/gitlab/web
```


# Configuration

There are different options for configuration:

Via Environment- variables or via query params:


## ENV

##### GITLAB_URL

The URL of your GitLab installation: http://git.example.com/

##### GITLAB_CHANNEL

The Room to which the gitlab messages get published. Use like this:

For HipChat

```
GITLAB_CHANNEL="xxxxxx_roomName@conf.hipchat.com"
```

For Let's Chat

```
GITLAB_CHANNEL="40b29e6ef217d12b00b8feff,86d1ce6ef217d61b00b8ab12"
```

##### GITLAB_DEBUG

Switches on debugging mode. Simply outputs more stuff :)


##### GITLAB_BRANCHES

Which branches should be pushed to chat.

Note: All push events are pushed to hubot but then the not required ones are discarded. If this is unset, all branch activity in the repo will be pushed to chat.

```
GITLAB_BRANCHES="master,develop"
```

##### GITLAB_SHOW_COMMITS_LIST

If the commits should be listed when code is pushed.


```
GITLAB_SHOW_COMMITS_LIST=0
```

##### GITLAB_SHOW_MERGE_DESCRIPTION

If the the merge request hook should also show the description. Useful for adapters like IRC where long descriptions can spam the channel

```
GITLAB_SHOW_MERGE_DESCRIPTION=0
```

## Query Params

##### targets

Same as ENV GITLAB_CHANNEL

```
?targets=%23room1,%23room2
```

###### Sampleurl

```
http://hubot.mydomain.com/gitlab/web?targets=%23room1,%23room2
```

##### branches

```
?branches=master,develop
```

###### Sampleurl

```
http://hubot.mydomain.com/gitlab/web?branches=develop,master
```

## Contributors

* [omribahumi](https://github.com/omribahumi) (original author)
* [spruce](https://github.com/spruce)


## License

hubot-gitlab-hooks is [MIT Licensed](https://github.com/spruce/hubot-gitlab-hooks/blob/master/LICENSE).
