FROM swift:latest

RUN git clone https://github.com/vknabel/sourcekite \
    && export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/lib/swift:/usr/lib \
    && ln -s /usr/lib/libsourcekitdInProc.so /usr/lib/sourcekitdInProc \
    && cd sourcekite && make install PREFIX=/usr/local -j2

WORKDIR /app
COPY . .