# repos-mirror-action
Auto mirror repos by GitHub Action

## Try Repo Mirror Sync
```yaml
name: <action-name>

on: 
  - push
  - delete

jobs:
  sync:
    runs-on: ubuntu-latest
    name: Repo Mirror Sync
    steps:
    - uses: actions/checkout@v3
    - name: Repo Mirror Sync
      uses: kubeservice-stack/repos-mirror-action@v1.0.1
      with:
        # Such as https://github.com/dongjiang1989/mirror-action.git
        target-url: <target-url>
        # Such as dongjiang1989
        target-username: <target-username>
        # You can store token in your project's 'Setting > Secrets' and reference the name here. Such as ${{ secrets.ACCESS_TOKEN }}
        target-token: <target-token>
```
