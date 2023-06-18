1. Создание образа:   

    ```docker
    docker build -t sqldb:1.0 .
    ```
    Создание контейнера:

    ```docker
    docker run --rm -d -p 5432:5432 --name testsql sqldb:1.0
    ```

2. Запуск psql в контейнере:

    ```docker
    docker exec -it testsql psql -U postgres 
    ```

3. Запуск контейнера с подключением volume для сохранения изменений в контейнере (где /data - папка на локальной машине, /var/lib/postgresql/data - папка в контейнере):

    ```docker
    docker run --rm -d -p 5432:5432 --name testsql -v /data:/var/lib/postgresql/data sqldb:1.0
    ```    