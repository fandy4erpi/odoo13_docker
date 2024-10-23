FROM odoo:13
ARG DEBIAN_FRONTEND=noninteractive
USER root
RUN apt-get update && \
    apt-get install -y python3-selenium \
    python3-dropbox \
    python3-paramiko \
    python3-roman \
    python3-oauthlib \
    python3-html2text \
    python3-pikepdf \
    python3-matplotlib \
    python3-pandas \
    && rm -rf /var/lib/apt/lists/*
RUN pip3 install --no-cache pyxlsb mpld3 packaging
COPY ee_latest/odoo /usr/lib/python3/dist-packages/odoo/
USER odoo