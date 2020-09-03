FROM swift:latest

# Install Vapor Toolbox
RUN git clone https://github.com/vapor/toolbox.git \
    && cd toolbox \
    && git checkout 18.2.2 \
    && make install -j2

WORKDIR /app
COPY . .