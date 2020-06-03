foo

Run CI in persistent docker containers so we don't futz with caching

Master service that spawns docker containers in a systemd service for each PR and master branch
while true:
    git pull
    run CI script
    sleep 5
Exit the container only when the PR is closed, and stop its systemd service

new branch
