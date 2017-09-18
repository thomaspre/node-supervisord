# node-supervisord
Docker run nodejs by supervisord

## Application logs

Get all logs by mounting a volume on /var/log/supervisor

## Test by command line with couchDB docker

``docker run -d --name thomaspre/nodejs-supervidord nodejs``
``docker run -d -p 8000:8000 --link=nodejs:nodejs -v /tmp/log/my_nodejs:/var/log/supervisor --name my_nodejs thomaspre/nodejs-supervisord``

Then open http://docker-machine-ip:8000/ to see nodejs interface plugged on this nodejs server and /tmp/log/my_nodejs for stdout and stderr

NodeJs will use by default nodejs:8000
