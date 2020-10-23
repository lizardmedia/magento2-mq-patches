## Overview ##

This repository contains patches for differen Magento Message Queue components. Issues fixed by these patches are currently under construction as PR's on official Magento 2 repository. The block taking full benefits from using Message Queue Framework, like queue arguments (DLX, message-ttl) or different consumer implementations.

- [Passing arguments for queues as expected #26966](https://github.com/magento/magento2/pull/26966)
- [Fix for queue numeric argument conversion #26967](https://github.com/magento/magento2/pull/26967)
- [Making message lock release possible #26968](https://github.com/magento/magento2/pull/26968)


## Usage ##
Just make sure to follow [official instruction for patch applying](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/composer.html).
This is sample configuration that can be used for ```composer.json``` file.

```
...
"extra": {
        ....
        "patches": {
            "magento/framework-message-queue": {
                "Passing arguments for queues as expected #26966": "patches/composer/26966.diff",
                "Making message lock release possible #26968": "patches/composer/26968-fmq.diff"
            },
            "magento/framework-amqp": {
                "Fix for queue numeric argument conversion #26967": "patches/composer/26967.diff"
            },
            "magento/module-message-queue": {
                "Making message lock release possible #26968": "patches/composer/26968-mq.diff"
            }
        }
	....
}
...
```


