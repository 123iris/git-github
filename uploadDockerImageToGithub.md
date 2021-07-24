# Upload docker image to github as packages

## 1. Creating Personal Access Token:

* The steps are followed from [here](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token)

1. Verify your email address, if it hasn't been verified yet.
2. In the upper-right corner of any page, click your profile photo, then click Settings.
3. In the left sidebar, click Developer settings.
4. In the left sidebar, click Personal access tokens.
5. Click Generate new token.
6. Give your token a descriptive name.


## 2. login

```
syed@syed-Latitude-3490:~/git/dockerImagePackages$ docker login docker.pkg.github.com -u  123iris -p PAT-token
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/syed/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded

```

## 3. Rename your docker image with github repo name as shown below

```
syed@syed-Latitude-3490:~/git/dockerImagePackages$ docker push docker.pkg.github.com/123iris/dockerimagepackages/eks-kinesis-example-main:v1
The push refers to repository [docker.pkg.github.com/123iris/dockerimagepackages/eks-kinesis-example-main]
c252bae552b7: Pushed 
564cde7c5ef2: Pushed 
ac140b625d91: Pushed 
eee580ffc61b: Pushed 
33e8713114f8: Pushed 
v1: digest: sha256:740ff2dc3e59733d61fc25316a841b20fea91c6a1f5280ce25ed289d2b0de452 size: 1372

```

## 4. Verify wether docker image is pushed as git repo packages

![dockerPushGithub.com.png](images/dockerPushGithub.com.png)
![dockerImageAsPackage.png](images/dockerImageAsPackage.png)


# Upload docker image as github container registry(ghcr)

## Follow step 1 & step 2 from above 

## Rename docker image to ghcr.io

```
syed@syed-Latitude-3490:~$ docker tag ubuntu:latest ghcr.io/123iris/dockerimagepackages:ubuntu1
syed@syed-Latitude-3490:~$ docker tag ubuntu:latest ghcr.io/123iris/dockerimagepackages:ubuntu2
```

## push docker image to github container registry

``` 
syed@syed-Latitude-3490:~$ docker login ghcr.io -u 123iris -p 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
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/syed/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
```
```
syed@syed-Latitude-3490:~$ docker push ghcr.io/123iris/dockerimagepackages:ubuntu1
The push refers to repository [ghcr.io/123iris/dockerimagepackages]
a70daca533d0: Pushed 
ubuntu1: digest: sha256:778fdd9f62a6d7c0e53a97489ab3db17738bc5c1acf09a18738a2a674025eae6 size: 529


syed@syed-Latitude-3490:~$ docker push ghcr.io/123iris/dockerimagepackages:ubuntu2
The push refers to repository [ghcr.io/123iris/dockerimagepackages]
a70daca533d0: Layer already exists 
ubuntu2: digest: sha256:778fdd9f62a6d7c0e53a97489ab3db17738bc5c1acf09a18738a2a674025eae6 size: 529
syed@syed-Latitude-3490:~$ 

```

## Verify in github

![dockerImageAsGithubContainerRegistry.png](images/dockerImageAsGithubContainerRegistry.png)
![dockerImageAsGithubContainerRegistryDetails.png](images/dockerImageAsGithubContainerRegistryDetails.png)
# References

1. [towardsdatascience.com](https://towardsdatascience.com/setting-up-github-package-registry-with-docker-and-golang-7a75a2533139)
1. [docs.github.com](https://docs.github.com/en/enterprise-server@3.0/packages/working-with-a-github-packages-registry/working-with-the-docker-registry)