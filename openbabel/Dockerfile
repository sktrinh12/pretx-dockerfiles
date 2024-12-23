FROM python:3.9

RUN apt-get update && apt-get install -y \
    openbabel \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

CMD ["/bin/bash"]
