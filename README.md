我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

kontainer-engine
========

A tool like docker-machine to provision kubernetes cluster for different cloud providers

## Building

`make`

## Usage

`kontainer-engine create --driver $driverName [OPTIONS] cluster-name`

`kontainer-engine inspect cluster-name`

`kontainer-engine ls`

`kontainer-engine update [OPTIONS] cluster-name`

`kontainer-engine rm cluster-name`

To see what driver create options it has , run
`kontainer-engine create --driver $driverName --help`

To see what update options for a cluster , run
`kontainer-engine update --help cluster-ame`

A serviceAccountToken which binds to the clusterAdmin is automatically created for you, to see what it is, run
`kontainer-engine inspect clusterName`

The current supported driver is gke(https://cloud.google.com/container-engine/)

Before running gke driver, make sure you have the credential. To get the credential, you can run any of the steps below

`gcloud auth login` or

`export GOOGLE_APPLICATION_CREDENTIALS=$HOME/gce-credentials.json` or 

`kontainer-engine create --driver gke --gke-credential-path /path/to/credential cluster-name`


## Running

`./bin/kontainer-engine`

## Tests

Run tests with:

```
    ./run_integration_tests
```

You must have Go and [Bats](https://github.com/sstephenson/bats) installed for the tests to run.

If you are adding new tests, note that they must have a `.bats` extension to be recognized by the runner.

## License
Copyright (c) 2014-2016 [Rancher Labs, Inc.](http://rancher.com)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
