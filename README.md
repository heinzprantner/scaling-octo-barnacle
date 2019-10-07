# scaling-octo-barnacle

work on aose 11

# Work Log

## Preparation

    GITHUB: Create Repository scaling-octo-barnacle
    HOST WS: git clone https://github.com/heinzprantner/scaling-octo-barnacle.git
    Bitbucket: Import Repository from github to MIRROR: scaling-octo-barnacle
    Bitbucket: Create FORK: hella-scaling-octo-barnacle

## Workspaces

### HOST WS SYNC

    git clone --mirror ssh://git@pluto.ham.hella.com:7999/aose/scaling-octo-barnacle.git
    cd scaling-octo-barnacle.git
    git remote add --mirror=push aose ssh://git@pluto.ham.hella.com:7999/aose/scaling-octo-barnacle.git
    git remote add --mirror=fetch github https://github.com/heinzprantner/scaling-octo-barnacle.git
    git remote update
    git push aose --mirror

## Test Steps

### Step 1

    GITHUB: add file src/main.c
    HOST WS: git sync -mirror GITHUB with MIRROR

### Step 2

    GITHUB: add file src/CmakeLists.txt
    HOST WS: git sync -mirror GITHUB with MIRROR
