### Application description

Dockerized Django with Postgres, Gunicorn, and Nginx

1. Build the images and run the containers:

    ```sh
    $ docker-compose -f docker-compose.yml up -d --build
    ```

    Test it out at [http://localhost:1337]. No mounted folders. To apply changes, the image must be re-built.

The app exposes its own metrics on /metrics path


Your task is to move this project to kubernetes platform and make it production-ready.

## Requirements
### Must-have requirements

1. All necessary kubernetes yaml manifests should be written
2. Monitoring through prometheus-operator
3. The app data should be persistent
4. Load-balancing and HA

### Nice-to-have requirements

5. Scaling improvements, considerations
6. Application performance improvements and/or considerations
7. Helm chart
8. AWS EKS demo (would be great if you can bootstrap eks with terraform) 
