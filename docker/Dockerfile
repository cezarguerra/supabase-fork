# Fazer build da imagem com o locale pt_BR.UTF-8

## docker build -t supabase-postgres-ptbr:latest .

FROM supabase/postgres:15.8.1.085

USER root
RUN apt-get update && \
    apt-get install -y locales && \
    locale-gen pt_BR.UTF-8 && \
    update-locale LANG=pt_BR.UTF-8 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
USER postgres