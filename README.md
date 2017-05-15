# docker-phinx
Dockerfile for container running PHP 7.1.4 and phinx, for running phinx related actions (migrate, seed, etc)

Phinx configuration file should be named "phinx.yml" and be in the phinx folder mapped to the container.

Parameters required to run the container:

phinx_command: command to send to phinx ("status" for a "phinx status" command)

folder with the phinx files: folder that contains the phinx files

Example of a status run:
docker run -e phinx_command=status -v c:/phinx:/phinx chaoticsound/docker-phinx:latest
