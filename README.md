##How to install TUS

Enter this command:

    wget https://github.com/tus/tusd/releases/download/v1.6.0/tusd_linux_amd64.tar.gz
    tar -xzvf tusd_linux_amd64.tar.gz
    mv tusd_linux_amd64.tar.gz/tusd /usr/local/bin/

now enter tmux and hit this command:

    tusd -base-path /var/nfs/ -upload-dir <your upload path> -port 35520 -behind-proxy
    
Note: add -behind-proxy flag only if you want to use it behind reverse proxies like haproxy or nginx    
    
then exit tmux using CTRL+b and then press d.
tus is now listening to http://0.0.0.0:35520<your upload path>
