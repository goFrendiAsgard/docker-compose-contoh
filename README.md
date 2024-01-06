# Setup

```bash
docker compose up  
docker exec -it airflow airflow users create --role Admin --username admin1 --email admin --firstname admin --lastname admin --password admin
```

# Konfigurasi Docker Compose

- Port

  ```yml
  ports:
    - <host-port>:<container-port>
  ```

- Volume

  ```yml
  ports:
    - <host-directory>:<container-directory>
  ```

# Perintah-perintah Troubleshooting

- Remote Access ke Container

  ```bash
  docker exec -it <nama-container> bash  

  # mengakses bash dengan hak akses root
  docker exec -u 0 -it <nama-container> bash  
  docker logs <nama-container>
  ```

- Telnet

  ```bash
  telnet [host-name [port]]
  ```

  Dari container dengan akses root (misal menggunakan apt):

  ```bash
  apt update --fix-missing
  apt install telnet
  ```

- Akses Container lain

  ```
  http://host.docker.internal:8081
  http://airflow:8080
  ```

- Profile
