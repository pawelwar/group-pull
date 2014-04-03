group pull
==========

The script allows you to update multiply repos by single request. You can define pattern of the directories which should be taken into consideration.

## Invokation
```bash
gpull [part of the directories name]
```

or just

```bash
gpull
```

## Example

###### Directorie structure:

```bash
tree .
├── test.configuration DONE
├── test.integrator DONE
├── test.libraries DONE
├── test.util-components DONE
├── test.authentication DONE
├── aaa.login-service
├── aaa.auth-service
└── priv.project-x
```

###### Invoke script:
gpull test

###### Result

```bash
* Update test.configuration DONE
* Update test.integrator DONE
* Update test.libraries DONE
* Update test.util-components fatal: Not possible to fast-forward, aborting.
* Update test.authentication DONE
```

Repositories: aaa.login-service, aaa.auth-service, priv.project-x was skipped.
