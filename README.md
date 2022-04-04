# manifest_cyclone

1.Now create a local_manifests dir and Copy the required manifests in that folder.

    mkdir .repo/local_manifests

    wget -O .repo/local_manifests/cyclone.xml 'https://raw.githubusercontent.com/ProjectCyclone/manifest_cyclone/main/cyclone.xml'
    
2.Then to sync up:

    repo sync -c -f --force-sync

OR, for those with limited bandwidth/storage:

    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
