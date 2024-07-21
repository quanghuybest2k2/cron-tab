FROM python:3.8
# 
WORKDIR /cronjob

# 
COPY . /cronjob

# 
RUN pip install --no-cache-dir --upgrade -r requirements.txt 

#
CMD ["python", "cron_run.py"]