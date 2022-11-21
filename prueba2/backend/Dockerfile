FROM python:3.7

WORKDIR /backend

COPY . .


RUN apt-get update \
    && apt-get install python-dev graphviz libgraphviz-dev pkg-config -y \
    && pip install --upgrade pip \
    && pip install pygraphviz 



RUN pip install -r requirements.txt


EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]