# server_setup
A quick guidance for setting up server using terminal


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

   *  Once you login into the remote server, try following command
      ```
      jupyter lab --ip 0.0.0.0 --port 8999 --no-browser --allow-root
      ```
   *  Then, open browser in your laptop and write `localhost:8999`. The jupyter lab is now on. 


## How to setup `git` in your remote server when you don't have `sudo` access.
   * Install `git` using conda
   ```
      conda install -c anaconda git
   ```
   * For the first time, to clone your repo in your system, you need to create `personal access token`. To generate the personal token please visit the [link](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).
   
   * After modification of any project/folder, use following commands 
      * git status
      * git add . OR git add --all 
      * git commit -m "your message"
      * git push 
      
   *  Useful links for Git.
      * https://stackoverflow.com/questions/38198165/when-to-use-git-add-and-when-git-add-a?noredirect=1&lq=1
      * https://stackoverflow.com/questions/7860751/git-fatal-unable-to-create-path-my-project-git-index-lock-file-exists
      * https://stackoverflow.com/questions/19573031/cant-push-to-github-because-of-large-file-which-i-already-deleted
      * https://medium.com/analytics-vidhya/tutorial-removing-large-files-from-git-78dbf4cf83a

      
   
## How to run `R` code using `Jupyter Lab`
   * ```conda config --add channels r```
   * ```conda config --add channels bioconda```
   * ```conda config --add channels conda-forge```
   
   * ```conda create -n r_env r-base bioconductor-biocinstaller``` 
   * ```conda install -c r r-essentials```
   * ```conda install -c conda-forge r r-essentials```
   * ```conda install -c conda-forge r-dplyr```
   * ```conda install -c conda-forge jupyterlab```
   
## How to install `bokeh` using conda
  conda install -c conda-forge ipympl
  conda install nodejs
  jupyter labextension install @jupyter-widgets/jupyterlab-manager
  jupyter lab build
  conda install bokeh

