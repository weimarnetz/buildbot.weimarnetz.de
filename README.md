# buildbot.weimarnetz.de

    # sudo -u buildbot -i 
    $ . venv/bin/activate 
    $ buildbot --help 
    $ buildbot-worker --help 
    
    $ tail -f /home/buildbot/master/twistd.log 
   
    /home/buildbot/{worker,master} 
    /home/buildbot/worker/builds 
    
 docs: http://docs.buildbot.net/current/
   
# Install 

    # apt install build-essential python3-dev python3-virtualenv
    # sudo -u buildbot -i 
    $ python3 -m venv venv 
    $ echo '. ~/venv/bin/activate' >> ~/.profile
    $ pip install wheel
    $ pip install 'buildbot[bundle]'

# Worker 

    $ buildbot-worker create-worker --umask=0o22 worker buildbot.weimarnetz.de <host> <pw>
