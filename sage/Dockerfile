FROM sagemath/sagemath:8.3

# Install git for development stuff
RUN sudo apt-get update && sudo apt-get install -y git

# copy over 
RUN git clone https://github.com/OpenDreamKit/MitM-Sage && \
    cd sage && \
    sage -pip install -e . --process-dependency-links --upgrade && \
    sage -pip install --upgrade git+https://github.com/OpenMath/py-openmath@odk-mitm-helpers && \
    sage -pip install --upgrade git+https://github.com/OpenMath/py-scscp

EXPOSE 26133
ENV SCSCP_HOST 0.0.0.0
CMD ["sage", "mitm/converting_server.py"]