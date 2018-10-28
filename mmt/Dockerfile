FROM kwarc/mmt:devel

# make sure all the archives are there
ENV MMT_ARCHIVES="MMT/urtheories@devel MMT/LFX@devel ODK/ODK"

# The custom mmtrc file to use
ADD mmtrc.custom /mmt/mmtrc.custom
ADD scscp.msl /mmt/scscp.msl

EXPOSE 26134
CMD ["-w", "--cfg", "/mmt/mmtrc.custom", "--file", "/mmt/scscp.msl"]