FROM python:3.14.3-slim

RUN pip install uv

WORKDIR /app

COPY pyproject.toml /app/
COPY requirements.txt /app/

RUN uv pip install --system -r requirements.txt

COPY . /app/

CMD ["uv", "run", "python", "encriptador.py", "--help"]
