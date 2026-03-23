- name: Configure kernel with SUSFS
  run: |
    cd kernel
    # SUSFS already copied
    echo "CONFIG_SUSFS=y" >> arch/arm64/configs/sushi_defconfig
    make ARCH=arm64 sushi_defconfig
