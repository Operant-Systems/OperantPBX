# OperantPBX
## Cloud native PBX system built for Kubernetes
___

### Our Goals

* Create a [Laravel](https://github.com/laravel/framework) app (monolith style but still scalable) that can control [FreeSWITCH](https://github.com/signalwire/freeswitch)
* Create a fully featured RESTful API to allow for 100% automation
* Get FreeSWITCH and dependencies fully working on [Kubernetes](https://github.com/kubernetes/kubernetes)
* Utilize [Routr](https://github.com/fonoster/routr) where it makes sense
* Feature parity with [FusionPBX](https://github.com/fusionpbx/fusionpbx) and allow custom add-ons
* Create Helm charts for everything and make OperantPBX easy to install on Kubernetes with a helm file
* Use either [Laravel Octane](https://github.com/laravel/octane) ([Swoole](https://github.com/swoole/swoole-src)) or [NGINX Unit](https://github.com/nginx/unit) to improve PHP performance
* Create SBC system that can secure, avoid NAT issues, and auto provision devices (This will probably be a different project)

### Challenges

* All configuration settings accessible via OperantPBX API should not require killing pods
* RTP/RTSP load balancing
* No StatefulSets to ensure high availability
* Secure ports with automated tools that can be maintained via OperantPBX API
* Many other things that we'll list here as we progress

### Why another PBX GUI (especially in PHP)

1. There's no HA open source PBX system working on Kubernetes as far as we know
2. PHP is still a great language and building RESTful APIs with Laravel will hopefully improve stability, readability, and security
3. We are disenchanted with closed source PBX systems being greedy and conducting unethical behavior (The number of this row gives hints)
4. We want to do right by our customers and provide them the best experience possible

### Supported "Clouds"

The list below might seem confusing as we're claiming this is cloud native, and yet we currently don't support any of the 3 largest US-based cloud providers. We plan on supporting all the cloud providers listed below, but we're going to start with what Operant Systems is using now. (Kubernetes + KVM + Ceph + MetalLB)

* [x] Generic on-prem
* [ ] AWS
* [ ] Azure
* [ ] GCP
* [ ] OpenStack

### How to Contribute

1. Review and agree to our [contributing guidelines](CONTRIBUTING.md)
2. Submit a PR with your changes and we'll review
