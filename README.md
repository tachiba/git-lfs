# Docker wrapped Git LFS

https://git-lfs.github.com/

## Example usage

If you run some which includes git-lfs tracked files on Cloud Build, you can checkout those files like this.

```
steps:
- name: tachiba/git-lfs
  args:
    - lfs
    - install
- name: tachiba/git-lfs
  entrypoint: ash
  args:
    - -c
    - |
      git clone -b $BRANCH_NAME --single-branch --depth=1 [GIT_REMOTE_URL]
```
