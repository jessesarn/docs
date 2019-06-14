---
title: MongoDB
menu:
  docs_0.12.0:
    identifier: mg-readme-mongodb
    name: MongoDB
    parent: mg-mongodb-guides
    weight: 10
menu_name: docs_0.12.0
section_menu_id: guides
url: /docs/0.12.0/guides/mongodb/
aliases:
  - /docs/0.12.0/guides/mongodb/README/
---

> New to KubeDB? Please start [here](/docs/concepts/README.md).

## Supported MongoDB Features

|                   Features                   | Availability |
| -------------------------------------------- | :----------: |
| Clustering - Sharding                        |   &#10003;   |
| Clustering - Replication                     |   &#10003;   |
| Persistent Volume                            |   &#10003;   |
| Instant Backup                               |   &#10003;   |
| Scheduled Backup                             |   &#10003;   |
| Initialize using Snapshot                    |   &#10003;   |
| Initialize using Script (\*.js and/or \*.sh) |   &#10003;   |
| Custom Configuration                         |   &#10003;   |
| Using Custom docker image                    |   &#10003;   |
| Builtin Prometheus Discovery                 |   &#10003;   |
| Using CoreOS Prometheus Operator             |   &#10003;   |

## Life Cycle of a MongoDB Object

<p align="center">
  <img alt="lifecycle"  src="/docs/images/mongodb/mgo-lifecycle.png">
</p>

## Supported MongoDB Versions

| KubeDB Version | Mongo:3.4 | Mongo:3.6 | Mongo:4.0.5, 4.0 | Mongo:4.1.7 |
| :------------: | :-------: | :-------: | :--------------: | :---------: |
| 0.1.0 - 0.7.0  | &#10007;  | &#10007;  |     &#10007;     |  &#10007;   |
|     0.8.0      | &#10003;  | &#10003;  |     &#10007;     |  &#10007;   |
|     0.9.0      | &#10003;  | &#10003;  |     &#10007;     |  &#10007;   |
|     0.10.0     | &#10003;  | &#10003;  |     &#10003;     |  &#10003;   |
|     0.11.0     | &#10003;  | &#10003;  |     &#10003;     |  &#10003;   |
|     0.12.0     | &#10003;  | &#10003;  |     &#10003;     |  &#10003;   |

## Supported MongoDB

Here, &#10003; means supported and &#10007; means deprecated.

|    NAME    | VERSION | KubeDB: 0.9.0 | KubeDB: 0.12.0 | KubeDB: 0.10.0 | KubeDB: 0.11.0 |
| :--------: | :-----: | :-----------: | :------------: | :------------: | :------------: |
|    3.4     |   3.4   |   &#10003;    |    &#10003;    |    &#10003;    |    &#10003;    |
|    3.6     |   3.6   |   &#10003;    |    &#10003;    |    &#10003;    |    &#10003;    |
| 4.0.5, 4.0 |  4.0.5  |   &#10007;    |    &#10007;    |    &#10003;    |    &#10003;    |
|   4.1.7    |  4.1.7  |   &#10007;    |    &#10007;    |    &#10003;    |    &#10003;    |

## Latest Supported MongoDBVersion Objects

Supported MongoDBVersion objects for KubeDB-0.13.0 release is,

```bash
$ kubectl get mongodbversions
NAME       VERSION   DB_IMAGE                DEPRECATED   AGE
3.4        3.4       kubedb/mongo:3.4        true         110m
3.4-v1     3.4       kubedb/mongo:3.4-v1     true         110m
3.4-v2     3.4       kubedb/mongo:3.4-v2     true         110m
3.4-v3     3.4       kubedb/mongo:3.4-v3                  110m
3.4-v4     3.4       kubedb/mongo:3.4-v4                  110m
3.6        3.6       kubedb/mongo:3.6        true         110m
3.6-v1     3.6       kubedb/mongo:3.6-v1     true         110m
3.6-v2     3.6       kubedb/mongo:3.6-v2     true         110m
3.6-v3     3.6       kubedb/mongo:3.6-v3                  110m
3.6-v4     3.6       kubedb/mongo:3.6-v4                  110m
4.0        4.0.5     kubedb/mongo:4.0        true         110m
4.0-v1     4.0.5     kubedb/mongo:4.0-v1                  110m
4.0-v2     4.0.5     kubedb/mongo:4.0-v2                  110m
4.0.5      4.0.5     kubedb/mongo:4.0.5      true         110m
4.0.5-v1   4.0.5     kubedb/mongo:4.0.5-v1                110m
4.0.5-v2   4.0.5     kubedb/mongo:4.0.5-v2                110m
4.1.7      4.1.7     kubedb/mongo:4.1.7      true         110m
4.1.7-v1   4.1.7     kubedb/mongo:4.1.7-v1                110m
4.1.7-v2   4.1.7     kubedb/mongo:4.1.7-v2                110m
```

Here `Deprecated: true` `MongoDBVersions` are not supported in latest release.

## External tools dependency

| Tool                                                   | Version |
| ------------------------------------------------------ | :-----: |
| [peer-finder](https://github.com/kmodules/peer-finder) | latest  |
| [osm](https://github.com/appscode/osm)                 |  0.9.1  |

## User Guide

- [Quickstart MongoDB](/docs/guides/mongodb/quickstart/quickstart.md) with KubeDB Operator.
- [MongoDB Replicaset](/docs/guides/mongodb/clustering/replicaset.md) with KubeDB Operator.
- [MongoDB Sharding](/docs/guides/mongodb/clustering/sharding.md) with KubeDB Operator.
- [Snapshot and Restore](/docs/guides/mongodb/snapshot/backup-and-restore.md) process of MongoDB databases using KubeDB.
- Take [Scheduled Snapshot](/docs/guides/mongodb/snapshot/scheduled-backup.md) of MongoDB databases using KubeDB.
- Initialize [MongoDB with Script](/docs/guides/mongodb/initialization/using-script.md).
- Initialize [MongoDB with Snapshot](/docs/guides/mongodb/initialization/using-snapshot.md).
- Start [MongoDB with Custom Config](/docs/guides/mongodb/configuration/using-custom-config.md).
- Monitor your MongoDB database with KubeDB using [out-of-the-box CoreOS Prometheus Operator](/docs/guides/mongodb/monitoring/using-coreos-prometheus-operator.md).
- Monitor your MongoDB database with KubeDB using [out-of-the-box builtin-Prometheus](/docs/guides/mongodb/monitoring/using-builtin-prometheus.md).
- Use [private Docker registry](/docs/guides/mongodb/private-registry/using-private-registry.md) to deploy MongoDB with KubeDB.
- Use [kubedb cli](/docs/guides/mongodb/cli/cli.md) to manage databases like kubectl for Kubernetes.
- Detail concepts of [MongoDB object](/docs/concepts/databases/mongodb.md).
- Detail concepts of [MongoDBVersion object](/docs/concepts/catalog/mongodb.md).
- Detail concepts of [Snapshot object](/docs/concepts/snapshot.md).
- Want to hack on KubeDB? Check our [contribution guidelines](/docs/CONTRIBUTING.md).
