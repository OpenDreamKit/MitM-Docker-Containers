FROM debian:stretch

# Install dependencies
RUN apt-get update \
    && apt-get install -y \
        git \
        python3-pip \
        libgmp3-dev \
        libsingular4-dev \
        pkg-config \
        singular \
    && pip3 install openmath scscp pysingular termcolor

# Put the repo into /app/
RUN git clone https://github.com/OpenDreamKit/MitM-Singular /app/
WORKDIR /app/

# expose the ports and run the script
EXPOSE 26135
ENV SCSCP_HOST 0.0.0.0
CMD [ "python3", "singular_server.py" ]