FROM dockersamples/examplevotingapp_vote:before
COPY ./app.py /app/app.py
EXPOSE 8000
CMD ["gunicorn", "app:app", "-b", "0.0.0.0:8000", "--log-file", "-", "--access-logfile", "-", "--workers", "4", "--keep-alive", "0"]