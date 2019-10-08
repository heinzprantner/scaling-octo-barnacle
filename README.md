# scaling-octo-barnacle

work on aose 11

# Work Log

## Preparation

    GITHUB: Create Repository scaling-octo-barnacle
    HOST WS GITHUB: git clone https://github.com/heinzprantner/scaling-octo-barnacle.git
    HOST WS SYNC: git clone --mirror https://github.com/heinzprantner/scaling-octo-barnacle.git
    Bitbucket: Import Repository from github to MIRROR: scaling-octo-barnacle
    Bitbucket: Create FORK: hella-scaling-octo-barnacle

## Workspaces

### HOST WS GITHUB

    git clone https://github.com/heinzprantner/scaling-octo-barnacle.git
    cd scaling-octo-barnacle

### HOST WS SYNC

    git clone --mirror ssh://git@pluto.ham.hella.com:7999/aose/scaling-octo-barnacle.git
    cd scaling-octo-barnacle.git
    git remote add --mirror=push aose ssh://git@pluto.ham.hella.com:7999/aose/scaling-octo-barnacle.git
    git remote add --mirror=fetch github https://github.com/heinzprantner/scaling-octo-barnacle.git
    git remote update --prune
    git push aose --mirror

## Test Steps

### Step 1

    HOST WS GITHUB: add file src/main.c
    HOST WS SYNC: git sync -mirror GITHUB with MIRROR

    CHECK: MIRROR and FORK are updated accordingly

### Step 2

    HOST WS GITHUB: add file src/CmakeLists.txt
    HOST WS SYNC: git sync -mirror GITHUB with MIRROR

    CHECK: MIRROR and FORK are updated accordingly

### Step 3

    HOST WS GITHUB: add branch
    HOST WS SYNC: git sync -mirror GITHUB with MIRROR

    CHECK: MIRROR and FORK are updated accordingly

### Step 4

    HOST WS GITHUB: add tag v0.0.1 (this step also includes moving the tag)
    HOST WS SYNC: git sync -mirror GITHUB with MIRROR

    CHECK: MIRROR and FORK are updated accordingly

### Step 5

    HOST WS GITHUB: git merge branch to master, delete branch
    HOST WS SYNC: git sync -mirror GITHUB with MIRROR

    CHECK: MIRROR and FORK are updated accordingly
