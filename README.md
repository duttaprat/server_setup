# server_setup
How to setup server using terminal


## How to setup `Jupyter Lab` in remote sever
   Before setting up `Jupyter Lab` in your remote server make sure your remote server has following prerequisites
   * `tunneling` facility to your server 
   * `Anaconda` should be install in your remote server. You can fiollow this [`Github repository`](https://github.com/duttaprat/AnacondaInstallation) for installing `Anaconda` in your remote server using terminal. 
   
   If you have the above requirements, following steps
   * Open terminal in your local system, paste the following command
      ```
      ssh -L <port number>:localhost:<port number>  <your username>@<remote server address>
      ```
      **_Here is an example_**
      ```
      ssh -L 8999:localhost:8999 pdutta@harrier1.cewit1.stonybr00k.edu
      ```
      In this case the port number is **8999**. You can use 8999 or your own port number(like **8080**). 

   *  Once you login into the remote server 



## How to setup `git` in your remote server when you don't have `sudo` access.
   * Install `git` using conda
   ```
      conda install -c anaconda git
   ```
   * 
   
