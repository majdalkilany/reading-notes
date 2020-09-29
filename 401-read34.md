# Configuring Django Settings: Best Practices

##### Managing Django Settings: Issues : 


**Different environments**. Usually, you have several environments: local, 
dev, ci, qa, staging, production, etc. Each environment can have its own 
specific settings (for example: DEBUG = True, more verbose logging, 
additional apps, some mocked data, etc). You need an approach that allows 
you to keep all these Django setting configurations.

**Sensitive data**. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.


**Sharing settings between team members**. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.


#### Setting Configuration: Different Approaches 

There is no built-in universal way to configure Django settings without 
hardcoding them. But books, open-source and work projects provide a lot of 
recommendations and approaches on how to do it best


* settings_local.py
The basic idea of this method is to extend all environment-specific
 settings in the settings_local.py file, which is ignored by VCS


 * Pros: 
 Secrets not in VCS.


* Cons: 

settings_local.py is not in VCS, so you can lose some of your Django environment settings.


The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.


You need to have settings_local.example (in VCS) to share the default configurations for developers.


#### Separate settings file for each environment


This is an extension of the previous approach. It allows you to keep all configurations in VCS and to share default settings between developers.


## How Does SSH Work

#### What is SSH
 SSH, or Secure Shell, is a remote administration protocol that allows 
 users to control and modify their remote servers over the Internet


#### How Does SSH Work

The SSH key command instructs your system that you want to open an 
encrypted Secure Shell Connection. {user} represents the account you want 
to access. For example, you may want to access the root user, which is 
basically synonymous for system administrator with complete rights to 
modify anything on the system. {host} refers to the computer you want to 
access. This can be an IP Address (e.g. 244.235.23.19) or a domain name (e.
g. www.xyzdomain.com).

