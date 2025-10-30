FROM almalinux:9
LABEL MAINTAINER="Kian-Tat Lim <ktl@slac.stanford.edu>"

ENV SUMMARY="Rubin Observatory base AlmaLinux 9 image for building software" \
    DESCRIPTION="This is the base image required for conda, lsstsw, and \
lsstinstall workflows"

LABEL name="lsstdm/scipipe-base:9" \
      version="9" \
      summary="$SUMMARY" \
      description="$DESCRIPTION" \
      io.k8s.description="$DESCRIPTION" \
      io.k8s.display-name="Rubin Observatory AlmaLinux 9 container"

RUN INSTALL_PKGS="git patch diffutils gnutls rclone" && \
    yum install -y --setopt=tsflags=nodocs ${INSTALL_PKGS} && \
    rpm -V ${INSTALL_PKGS} && \
    yum -y clean all --enablerepo='*'
