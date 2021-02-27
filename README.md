TWRP Device Tree for Samsung Galaxy J4
• Build Type : Unofficial

• Status : STABLE

• Developer : BlackRomsDev(Lautaro Cepeda)

How to Install?
• Download latest zip file in 'Release' tab

• Extract downloaded zip, and you'll find 'recovery.img'

• Go to any custom recovery, since we'll install recovery in recovery

• Flash recovery.img as Recovery

• Reboot to recovery

• Done!

[DEV ONLY!] How To Build
[1] Download Source • Prepare your environment and dependencies, then :

mkdir twrp && cd twrp

repo init -u --depth=1 https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni -b twrp-8.1

repo sync
[2] Download the tree

mkdir -p device/samsung && cd device/samsung

git clone https://github.com/blackwidowroms/TWRP_J4 j4ltejx
cd ../..

[3] Build it

source build/envsetup.sh

export ALLOW_MISSING_DEPENDENCIES=true

lunch omni_j4ltejx-eng

mka recoveryimage

The builded recovery is in out/target/product/j4ltejx
