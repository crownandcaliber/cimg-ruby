# vim:set ft=dockerfile:

FROM cimg/ruby:2.7.5

LABEL maintainer="Community & Partner Engineering Team <community-partner@circleci.com>"

# Dockerfile will pull the latest LTS release from cimg-node.
RUN curl -L -o node.tar.xz "https://nodejs.org/dist/v12.9.1/node-v12.9.1-linux-x64.tar.xz" && \
      sudo tar -xJf node.tar.xz -C /usr/local --strip-components=1 && \
      rm node.tar.xz && \
      sudo ln -s /usr/local/bin/node /usr/local/bin/nodejs

ENV YARN_VERSION 1.22.5
RUN curl -L -o yarn.tar.gz "https://yarnpkg.com/downloads/${YARN_VERSION}/yarn-v${YARN_VERSION}.tar.gz" && \
      sudo tar -xzf yarn.tar.gz -C /opt/ && \
      rm yarn.tar.gz && \
      sudo ln -s /opt/yarn-v${YARN_VERSION}/bin/yarn /usr/local/bin/yarn && \
      sudo ln -s /opt/yarn-v${YARN_VERSION}/bin/yarnpkg /usr/local/bin/yarnpkg
