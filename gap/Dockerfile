FROM gapsystem/gap-docker-stable-4.10

# Install the MitM package
RUN /bin/bash -c "git clone https://github.com/gap-packages/MathInTheMiddle ${GAP_HOME}/pkg/MathInTheMiddle"

# port for scscp
EXPOSE 26133

# Add the script to start the server
ADD scscp.g /home/gap/scscp.g
CMD ["/bin/bash", "-c", "$GAP_HOME/bin/gap.sh -A /home/gap/scscp.g"]