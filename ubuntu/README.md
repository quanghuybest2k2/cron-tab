## prepare

Open `crontab` file and switch `CRLF` to `LF`

## run

```shell
docker compose up -d --build
```

```shell
docker exec -it cron-job bash
```

## example run job

```bash
* * * * * python3 /app/hello.py >> /var/log/cron.log
```

## giải thích

Detailed Explanation
`* * * * *`

`*`: Theo thứ tự: Phút: (0-59), Giờ: (0-23), Ngày trong tháng: (1-31), Tháng: (1-12), và Ngày trong tuần: (0-6), 0 là Chủ nhật.
`python3 /app/hello.py`:

Executes the Python file located at /app/hello.py.
`>>`:

Appends to the end of the file without overwriting.

## config

`crontab -e: Mở trình soạn thảo crontab để thêm hoặc sửa cronjob.` <br/>
`service cron restart: Khởi động lại dịch vụ cron để áp dụng thay đổi.`

## service cron

```shell
service cron status
```

```shell
service cron start
```

```shell
service cron stop
```
