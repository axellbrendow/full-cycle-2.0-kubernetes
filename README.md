# full-cycle-2.0-kubernetes

Files I produced during the Kubernetes classes of the Full Cycle 2.0 [course](https://drive.google.com/file/d/1MdN-qK_8Pfg6YI3TSfSa5_2-FHmqGxEP/view?usp=sharing)

# Stress test

```sh
kubectl run -it fortio --rm --image=fortio/fortio -- load -qps 800 -t 120s -c 70 "http://goserver/healthz"
```
