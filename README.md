# Solution (Must-have part)

Dock^W Kuberized Django with Postgres, Gunicorn, and Nginx

1. Build "web" and "nginx" (or use already builded images after docker-compose build) images and push to registry [hub.docker.com](https://hub.docker.com/u/vinduzyatnik) as

    ```sh
    vinduzyatnik/k8s-sre-task_nginx
    vinduzyatnik/k8s-sre-task_web
    ```

2. Spin up docker-desktop kubernetes one node cluster.


3. Install "ingress-nginx" and "kube-prometheus-stack" helm charts.


![picture](img/start_conditions.png)

4. Deploy all inside this repo via

    ```sh
    $ kubectl apply -k ./
    ```

    Test it out at [http://localhost].

![picture](img/app.png)

6. Metrics available in prometheus.


![picture](img/prom.png)

![picture](img/metrics.png)

5. PROFIT!!!!!11

UPD 4.07.2021

1. db user and pass moved to secret
2. create kustomization file
3. add helm 

Deploying using helm

    ```sh
    $ helm install <name> web-app
    ```

    OR

    ```sh
    $ helm install web-app --generate-name
    ```