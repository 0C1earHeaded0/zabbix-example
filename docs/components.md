- # Zabbix агент (<a href='https://hub.docker.com/r/zabbix/zabbix-agent/'>zabbix/zabbix-agent</a>)

        Сидит на наблюдаемых целях, собирает статистику и метрики, формирует отчёты и <>либо сам отправляет на сервер, либо в ответ на запрос заббикс-сервера.

- # Zabbix сервер

        Мозг, работает с базой и триггерами, мониторит, общается с прокси и агентами, кидает алерты.

    - ## MySQL (<a href='https://hub.docker.com/r/zabbix/zabbix-server-mysql/'>zabbix/zabbix-server-mysql</a>)
    - ## PostgreSQL (<a href='https://hub.docker.com/r/zabbix/zabbix-server-pgsql/'>zabbix/zabbix-server-pgsql</a>)


- # Zabbix веб-интерфейс

        Вебка, позволяющая настраивать мониторинг, алертинг и непосредственно следить за работой наблюдаемых серверов через дашборды.

    - ## Apache2 + ... :
        - ### MySQL (<a href='https://hub.docker.com/r/zabbix/zabbix-web-apache-mysql/'>zabbix/zabbix-web-apache-mysql</a>)
        - ### PostgreSQL (<a href='https://hub.docker.com/r/zabbix/zabbix-web-apache-pgsql/'>zabbix/zabbix-web-apache-pgsql</a>)
    - ## Nginx + ... :
        - ### MySQL (<a href='https://hub.docker.com/r/zabbix/zabbix-web-nginx-mysql/'>zabbix/zabbix-web-nginx-mysql</a>)
        - ### PostgreSQL (<a href='https://hub.docker.com/r/zabbix/zabbix-web-nginx-pgsql/'>zabbix/zabbix-web-nginx-pgsql</a>)

- # Zabbix прокси
    
        Зам главного сервера, может сам опросить агентов и временно сохранить метрики к себе, но не может в триггеры и алерты.

    - ## SQLite3 (<a href='https://hub.docker.com/r/zabbix/zabbix-proxy-sqlite3/'>zabbix/zabbix-proxy-sqlite3</a>)
    - ## MySQL (<a href='https://hub.docker.com/r/zabbix/zabbix-proxy-mysql/'>zabbix/zabbix-proxy-mysql</a>)

- # Zabbix Java Gateway (<a href='https://hub.docker.com/r/zabbix/zabbix-java-gateway/'>zabbix/zabbix-java-gateway</a>)

        Позволяет "нативно" следить за состоянием JVM (Java Virtual Machine) через технологию JMX (Java Management Extensions)