# Atlassian JIRA Software in a Docker container

## Build

To build this image

    docker build -t your-name/jira-software .

## Quick start

To start a JIRA Software instance:

    docker run -d -p 8080:8080 your-name/jira-software

Navigate to http://localhost:8080 and do configuration

## Jira Software with Postgres

Start postgres docker container

    docker run -d --name jiradb-postgres  \
    -e POSTGRES_USER=jira \
    -e POSTGRES_DB=jira \
    -e POSTGRES_PASSWORD=jira \
    lopezs/postgres

This creates a docker container *jiradb-postgres* that we can link to to a Jira Software instance, which we will name *jira7*:

    docker run -d -p 8080:8080 --link jiradb-postgres:postgres --name jira7 your-name/jira-software
