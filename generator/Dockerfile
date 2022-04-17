FROM python:alpine3.15

RUN adduser -D generator
USER generator
WORKDIR /home/generator

COPY --chown=generator:generator . .

ENV FLASK_APP=generator.py
ENV FLASK_ENV=development
ENV PATH="/home/generator/.local/bin:${PATH}"

RUN pip install --user -r requirements.txt

EXPOSE 8000

CMD ["python", "-m", "flask", "run", "--host=0.0.0.0", "--port=8000"]