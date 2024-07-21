# run

```shell
docker compose up -d --build
```

```shell
docker exec -it python-cronjob bash
```

## example run job

```bash
* * * * * python hello.py >> cron.log
```

## config

`crontab -e: Mở trình soạn thảo crontab để thêm hoặc sửa cronjob.` <br/>
`service cron restart: Khởi động lại dịch vụ cron để áp dụng thay đổi.`
