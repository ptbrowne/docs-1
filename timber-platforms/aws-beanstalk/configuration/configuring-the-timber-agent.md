# Configuring the Timber Agent

[The Timber agent](/platforms/other/timber-agent) is what powers Elastic Beanstalk log delivery in the background. As a result, most configurations of Timber in the ElasticBeanstalk environment is done by [configuring the Timber agent](/platforms/other/timber-agent/configuration-file).


## How to

At the top of your Timber ebextension file you'll notice an entry for `/etc/timber.toml`. Simply modify the contents of this file based on the [available Timber agent configuration options](/platforms/other/timber-agent/configuration-file):

```toml
---
files:
  "/etc/timber.toml":
    mode: "000640"
    owner: root
    group: root
    encoding: plain
    content: |
      # insert configuration options here
```
