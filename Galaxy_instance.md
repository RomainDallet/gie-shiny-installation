Install Galaxy instance (Linux)
===============================

Requirements :

- Python 2.7
- PostgreSQL
- uWSGI (for v18.01)

Packages needed :

- pip (already installed if you're using Python 2 >=2.7.9 or Python 3 >=3.4)
- [conda](https://conda.io/docs/user-guide/install/linux.html), to install tools


Make sure Git is installed. If not, install it with the following command :

`apt-get install git`


Start to clone the Galaxy repository :

`git clone -b release_17.09 https://github.com/galaxyproject/galaxy.git`


To start your Galaxy instance :

```
cd galaxy/
./run.sh
```

After a few minutes of installation, our galaxy instance should be running on `http://localhost:8080`


Next, make yourself an administrator.

- Create a user account using the Galaxy User Interface (Login or Register -> Register)
- Copy the provided `galaxy.ini.sample` : `cp $GALAXY_PATH/config/galaxy.ini.sample $GALAXY_PATH/config/galaxy.ini`
- Modify `$GALAXY_PATH/config/galaxy.ini` to include your email as an admin by modifying the line `admin_users = $YOUR_EMAIL`
- (Re)start Galaxy (`./run.sh`)

If everything works, you should have a Admin tab on you Galaxy User Interface.