# 1 -- clone repository

    git clone https://github.com/jweiss63/ngctf && cd ngctf


# 2 -- build container [ takes 5-10 minutes ]

    sudo docker build -t s9256-container:v0 .


# 3 -- launch/run the container [ auto starts jupyter notebook ]

    sudo docker run --runtime=nvidia -it --rm -p 8888:8888 s9256-container:v0


# 4 -- create a port map / ssh-tunnel to the container 
 	
    ssh -L 8888:localhost:8888 remote_user@remote_host


# 5 -- launch demo from browser [ on your local machine ]

    use a browser [ firefox is recommended ] and navigate to 127.0.0.1:8888
    this should open a jupyter lab/notebook session
    navigate to the /S9256-session directory
    click on S9256-session.ipynb to launch the demo

