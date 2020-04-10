FROM centos:8
LABEL MAINTAINER Brian Van Klaveren <bvan@slac.stanford.edu>

ENV SUMMARY="Rubin Observatory base centos 8 image for building software" \
    DESCRIPTION="This is the base image required for conda, lsstsw, and \
newinstall workflows"

LABEL name="lsstdm/scipipe-base:8" \
      version="8" \
      summary="$SUMMARY" \
      description="$DESCRIPTION" \
      io.k8s.description="$DESCRIPTION" \
      io.k8s.display-name="Rubin Observatory centos 8 container" 

RUN INSTALL_PKGS="git patch" && \
    yum install -y --setopt=tsflags=nodocs ${INSTALL_PKGS} && \
    rpm -V ${INSTALL_PKGS} && \
    yum -y clean all --enablerepo='*'
