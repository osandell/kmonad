
I followed the discussion here regarding problems with the "§" key: https://github.com/kmonad/kmonad/issues/106

This was fixed in the keycode-refactor branch which was not yet merged at the time of pulling the repo (2023-07-16).

What I did was just to branch out from keycode-refactor and made a small adjustment to make it run.

Built it with:
`stack build --flag kmonad:dext --extra-include-dirs=c_src/mac/Karabiner-DriverKit-VirtualHIDDevice/include/pqrs/karabiner/driverkit:c_src/mac/Karabiner-DriverKit-VirtualHIDDevice/src/Client/vendor/include`


Also followed these instructions:

`Install the already build and signed dext package

To install the dext as a signed binary, initialize the dext git submodule, install the extension, and activate the extension.

  $ git clone --recursive https://github.com/kmonad/kmonad.git

  $ cd kmonad/
  $ open c_src/mac/Karabiner-DriverKit-VirtualHIDDevice/dist/Karabiner-DriverKit-VirtualHIDDevice-1.15.0.pkg

  $ /Applications/.Karabiner-VirtualHIDDevice-Manager.app/Contents/MacOS/Karabiner-VirtualHIDDevice-Manager activate

Note: If activation failed (e.g. because a newer version is already installed), replace activate in the above command with forceActivate and try again.`
