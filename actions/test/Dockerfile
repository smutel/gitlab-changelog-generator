FROM python:3.7-alpine

LABEL "com.github.actions.name"="test"
LABEL "com.github.actions.description"="Runs unit tests"
LABEL "com.github.actions.icon"="terminal"
LABEL "com.github.actions.color"="black"

LABEL "repository"="https://github.com/stuartmccoll/gitlab-changelog-generator"
LABEL "maintainer"="Stuart McColl <it@stuartmccoll.co.uk>"

RUN apk add --no-cache bash build-base gcc
RUN pip install --upgrade pip
RUN pip install pytest mock requests python-dateutil
RUN python --version ; pip --version ; pytest --version

COPY entrypoint.sh /
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]