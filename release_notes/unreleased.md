**Unreleased**

* Fail feed downloads that exceed the connector's network timeout.

* Limit each feed entry's linked-page download to 50 MiB and the connector's network timeout.

* Key RSS container identifiers with a per-asset secret to prevent pre-created container collisions.

* Defer future-dated feed entries and reset future poll checkpoints before selecting new entries.

* Extract IOC URLs from HTML src attributes in feed-linked pages.
