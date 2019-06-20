# Changelog

## 0.35

- Update keepalived to v2.0.16
- [#97](https://github.com/aledbf/kube-keepalived-vip/issues/97) Don't remove VIPs on reload

## 0.34

- Only watch one configmap
- [#81](https://github.com/aledbf/kube-keepalived-vip/issues/91) Reset IPVS after API client init 
- [#92](https://github.com/aledbf/kube-keepalived-vip/pull/92) Add flag to make ipvs reset optional

## 0.33

- Update keepalived to v2.0.15
- Remove check that avoids the render of the template and comparison of the md5
- [#72](https://github.com/aledbf/kube-keepalived-vip/pull/72) nopreempt is set along with priority weights?
- [#87](https://github.com/aledbf/kube-keepalived-vip/issues/87) keepalived-vip v0.30 cannot be aware of the backend pod scaling

## 0.32

- Update keepalived to v2.0.11
- [#79](https://github.com/aledbf/kube-keepalived-vip/pull/79) add notify script via environment variable

## 0.31

- [#71](https://github.com/aledbf/kube-keepalived-vip/pull/71) Add health check
- [#75](https://github.com/aledbf/kube-keepalived-vip/pull/75) Fix race condition crash on startup

## 0.30

- Update keepalived to v2.0.10
- [#68](https://github.com/aledbf/kube-keepalived-vip/pull/68) Cleanup VIPs on startup
- [#69](https://github.com/aledbf/kube-keepalived-vip/pull/69) Start kube-keepalived-vip via dumb-init

## 0.29

- Disable resync period

## 0.28

- Update keepalived to v2.0.7
- Update Kubernetes dependencies to 1.11.3

## 0.27

- Update keepalived to v1.4.4

## 0.26

- Fix keepalived SIGSEGV in k8s 1.9.x

## 0.25

- Update go dependencies
- [x] [#8](https://github.com/aledbf/kube-keepalived-vip/pull/35) Fix keepalived dependencies

## 0.24

- Update keepalived to v1.4.0
- Change docker base image to gcr.io/google-containers/debian-base-amd64:0.3

## 0.23

- Update keepalived to v1.3.9

## 0.22

- Update keepalived to v1.3.7

## 0.21

- Fix template error

## 0.20

- [x] [#8](https://github.com/aledbf/kube-keepalived-vip/pull/8) Fix keepalived config file error when there are no services
- [x] [#9](https://github.com/aledbf/kube-keepalived-vip/pull/9) Add support for travis-ci
- [x] [#10](https://github.com/aledbf/kube-keepalived-vip/pull/10) Add badges
- [x] [#11](https://github.com/aledbf/kube-keepalived-vip/pull/11) Fix badges
- [x] [#17](https://github.com/aledbf/kube-keepalived-vip/pull/17) Remove unnecessary backquote and space
- [x] [#18](https://github.com/aledbf/kube-keepalived-vip/pull/18) VRID flag not supported in keepalived.tmpl
- [x] [#19](https://github.com/aledbf/kube-keepalived-vip/pull/19) Use vrid flag in template

## 0.17

- Cleanup
- Configmap update detection

## 0.16

- Fix DR mode issue

## 0.15

- Update keepalived to 1.3.6
- Update go dependencies
- Migrate to client-go

## 0.10

- Add proxy mode
- Update keepalived to 1.3.2
- Update godeps
- Fix network interface detection issues

## 0.9

- Update godeps
- Update keepalived to 1.2.24

## 0.8

- Update godeps - required by kubernetes/kubernetes#31396
- Update ubuntu-slim to 0.4

## 0.7

- Update keepalived to 1.2.23
- Use delayed queue
- Avoid sync without a reachable master

## 0.6

- Update keepalived to 1.2.21

## 0.5

- Respect nodeSelector to build the list of peer nodes when --use-unicast is true
- Add support for UDP services

## 0.4

- Update keepalived to 1.2.20
- Use iptables parameter to not respond on addresses that it does not own
- Replace annotations with ConfigMap to specify services and IP addresses
- Avoid unnecessary reloads if the configuration did not change
- The parameter --password was removed because is not supported in vrrp v3
