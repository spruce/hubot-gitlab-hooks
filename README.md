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


#Configuration

There are different options for configuration:

Via Environment- variables or via query params:


##ENV

#####GITLAB_CHANNEL

The Room to which the gitlab messages get published. Use like this:

For HipChat

```
GITLAB_CHANNEL="xxxxxx_roomName@conf.hipchat.com"
```

#####GITLAB_DEBUG

Switches on debugging mode. Simply outputs more stuff :)


#####GITLAB_BRANCHES

Which branches should be pushed to chat.

Note: all push events are pushed to hubot but then the not required ones are discarded.

```
GITLAB_BRANCHES="master,develop"
```


##Query Params

#####targets

Same as ENV GITLAB_CHANNEL

```
?targets=%23room1,%23room2
```

######Sampleurl

```
http://hubot.mydomain.com/gitlab/web?targets=%23room1,%23room2
```

#####branches

```
?branches=master,develop
```

######Sampleurl

```
http://hubot.mydomain.com/gitlab/web?branches=develop,master
```

## Contributors

* [omribahumi](https://github.com/omribahumi) (original author)
* [spruce](https://github.com/spruce)


## License

hubot-gitlab-hooks is [MIT Licensed](https://github.com/ember-cli/ember-cli/blob/master/LICENSE.md).
