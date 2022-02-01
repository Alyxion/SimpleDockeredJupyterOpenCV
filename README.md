# A simple Jupyter working environment in Docker

## Installation

* **Requirements**
  * An up to date Docker and Docker-Compose installation
   * A Linux environment such as Ubuntu. - WSL2 works fine too
* Copy the file `env.template` to `.env`
* Open it in an editor
* Adjust the value PROJECT_DIR to the path in which the projects are located you would like to work with
* Open a terminal in this project's main folder
* Execute `sudo docker-compose up --build --remove-orphans`
* Open the url http://127.0.0.1:5005 in your browser

If you need additional packages just add them in the file `jupyteropencv/requirements.txt`.

Have fun!