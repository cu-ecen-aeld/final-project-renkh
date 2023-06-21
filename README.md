# final-project-renkh
final-project-renkh created by GitHub Classroom

Link to the project wiki page: https://github.com/cu-ecen-aeld/final-project-renkh/wiki/Project-Overview

## Getting Started
1. Install Google Repo command.

    Download the Repo tool on your system:

        $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > repo
        $ chmod a+x repo
        $ sudo mv repo /usr/local/bin/

2. Initialize the Repo client.

    Create an empty directory to hold the working files:

        $ cd ${HOME}/${WORK_DIR}
        $ mkdir final-project-renkh
        $ cd final-project-renkh

    Initialize the Repo:

        $ repo init -u ssh://git@github.com/cu-ecen-aeld/final-project-renkh -b master

    A successful initialization will end with a message stating that Repo is
    initialized in your working directory. Your client directory should now
    contain a `.repo` directory where files such as the manifest will be kept.

3. Fetch all repositories:

        $ repo sync

    This command will fetch the Yocto layers specified in the manifest.

4. Source the Yocto enviroment:

        $ source ./setup-env

    This copies default configuration information into the `build/conf`
    directory and sets up some environment variables for OpenEmbedded.

5. Build an image:

        $ bitbake core-image-minimal

    This process takes a really long time depending on the system's resources.
    Bitbake will download source code, build packages, and generate the final
    image.
