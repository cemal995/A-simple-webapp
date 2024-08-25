# Docker ve Kubernetes ile Node.js Web Uygulaması

## Genel Bakış
Bu proje, basit bir Node.js web uygulamasını Docker ve Kubernetes kullanarak nasıl konteynerize edip dağıtacağınızı gösterir.

## Kurulum

1. **Depoyu Klonlayın:**

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2. **Docker İmajını Oluşturun ve Yükleyin:**

    ```bash
    docker build -t <your_dockerhub_username>/webapp .
    docker push <your_dockerhub_username>/webapp
    ```

3. **Kubernetes Dağıtımını Yapın:**

    ```bash
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    ```

4. **Uygulamayı Erişin:**

    - Pod’ların durumunu kontrol edin:

      ```bash
      kubectl get pods
      ```

    - Servis IP adresini alın:

      ```bash
      minikube service nodejs-app-service
      ```

    - Web tarayıcınızda veya `curl` komutuyla erişin:

      ```bash
      curl http://<LoadBalancer_IP>
      ```

## Dosyalar

- **Dockerfile:** Node.js uygulamasını konteynerize eder.
- **deployment.yaml:** Kubernetes Deployment konfigürasyonu.
- **service.yaml:** Kubernetes Service konfigürasyonu.


**Yazar:** Cemalhan Alptekin
