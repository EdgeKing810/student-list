FROM python:2.7-stretch

# Maintainer has been deprecated
LABEL Maintainer="Kishan Takoordyal <kishan@kinesis.games>"

RUN apt-get update -y && \
    apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y

RUN pip install flask flask_httpauth flask_simpleldap python-dotenv

# Won't be able to and doesn't make sense to make a volume at "/" (root)
VOLUME [ "/data/" ]

EXPOSE 5000

CMD [ "python", "/data/student_age.py" ]
