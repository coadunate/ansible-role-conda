Conda
=========

This is a template role which installs Conda into the targeted Virtual Machine.

Requirements
------------

N/a

Role Variables
--------------

N/a

Dependencies
------------

- [coadunate.devtools](https://github.com/coadunate/ansible-role-devtools) 

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: coadunate.conda }


Working with Conda
------------------

- ### Getting python 3.6.2 in your conda environment
    With conda, you can create, export, list, remove and update environments that have different versions of Python and/or packages installed in them. Switching or moving between environments is called activating the environment. You can also share an environment file.
    
    In this example we are going to create an enviornment with python verison 3.6.2 and we're going to activate and deactive the enviornment.
    
    1. Checking the available versions of python.
    
        Before creating the the enviornment, we first need to check the versions of python that are available in conda. In order to do that, we need to use following command:
        
            conda search "^python$"
        
        And the result of this command is as follows:
        
            $ conda search "^python$"
            Fetching package metadata .........
            python                       1.0.1                         0  defaults
                                        2.6.8                         1  defaults
                                        2.6.8                         2  defaults
                                        2.6.8                         3  defaults
                                        ...                              ...
                                        ...                              ...
                                        ...                              ...
                                        ...                              ...
                                        3.6.0                         0  defaults
                                        3.6.1                         0  defaults
                                     *  3.6.1                         2  defaults
                                        3.6.2                         0  defaults
                                        
                                        

    
    2. Creating an enviornment.
    
        In order to create an environment, we are going to use the following command
        
            conda create --name myenv
        
        We have to specify the version of python that is going to be used by the environment, therefore we can alter the command as follows:
        
            conda create --name myenv python=x.x  // where myenv is the name of environment and x.x is the version of python
            
    3.  (De)Activating the enviornment.
    
        In order to activate the environment, we use the following command:
        
            source activate myenv // where myenv is the name of the enviroment
        
        In order to deactivate the environment,we use the following command:
        
            source deactivate myenv // where myenv is the name of the environment
            
       


License
-------

CC-BY

Author Information
------------------

Coadunate Organization
