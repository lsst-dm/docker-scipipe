FROM centos:7
LABEL MAINTAINER Brian Van Klaveren <bvan@slac.stanford.edu>

ENV SUMMARY="Rubin Observatory Base CentOS 7 image for building software" \
    DESCRIPTION="This is the base image required for conda, lsstsw, and \
newinstall workflows"

LABEL name="lsstdm/scipipe-base:7" \
      version="7" \
      summary="$SUMMARY" \
      description="$DESCRIPTION" \
      io.k7s.description="$DESCRIPTION" \
      io.k7s.display-name="Rubin Observatory centos 7 container" 

RUN INSTALL_PKGS="git patch" && \
    yum install -y --setopt=tsflags=nodocs $INSTALL_PKGS && \
    rpm -V $INSTALL_PKGS && \
    yum -y clean all --enablerepo='*'
