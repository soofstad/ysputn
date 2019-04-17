FROM python:alpine3.9
ENV FLASK_APP=/src/app.py
WORKDIR /src
RUN pip install pipenv
COPY Pipfile* ./
RUN pipenv install --system --dev --deploy
COPY . /src
CMD ["python", "/src/app.py"]