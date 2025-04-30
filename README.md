# openwrtKAS
automated repo allocator for meta-openwrt based projects

build steps:

step 0:
clone Siemens KAS

git clone https://github.com/siemens/kas.git

create python3 venvironment

python3 -m venv py3.env

step 1:
build recipe

source python3 venv

source py3.env/bin/activate

just distrolles openembedded core-image-minimal
 kas build kas/distroless-kirkstone-config.yml

or openwrt for qemuarm kirkstone openembedded
 kas build kas/openwrt-arm-kirkstone-config.yml

or openwrt-base packages set for kirtstone openembedded
 kas build kas/openwrt-base-kirkstone-config.yml

or openwrt-image-full packages set for kirtstone openembedded
 kas build kas/openwrt-full-kirkstone-config.yml

or openwrt-image-minimal packages set for kirtstone openembedded
 kas build kas/openwrt-kirkstone-config.yml

or including linaro toolchain:
 kas build kas/openwrt-linaro-kirkstone-config.yml

or openwrt-full packages set for kirtstone openembedded including linaro toolchain:
 kas build kas/openwrt-full-linaro-kirkstone-config.yml
