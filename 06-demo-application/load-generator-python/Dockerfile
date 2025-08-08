FROM python:3.12-slim AS production

# Configure pip to use Chinese mirror (Tsinghua University)
RUN pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple \
    && pip config set install.trusted-host pypi.tuna.tsinghua.edu.cn

# Install requests package using the mirror
RUN pip install --no-cache-dir requests==2.32.2

COPY . .
CMD ["python", "main.py"]
