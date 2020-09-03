FROM swift:latest

# Install Sourcekite for LSP
RUN git clone https://github.com/vknabel/sourcekite \
    && export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/lib/swift:/usr/lib \
    && ln -s /usr/lib/libsourcekitdInProc.so /usr/lib/sourcekitdInProc \
    && cd sourcekite && make install PREFIX=/usr/local -j2

# Install Vapor Toolbox
RUN git clone https://github.com/vapor/toolbox.git \
    && cd toolbox \
    && git checkout 18.2.2 \
    && make install -j2

WORKDIR /app
COPY . .