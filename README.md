# Slice (SDDM Theme)

Simple dark SDDM theme.

[![Theme preview (YouTube)](http://img.youtube.com/vi/y2zzlDdJTUU/0.jpg)](https://youtu.be/y2zzlDdJTUU)

## Installing

1. Install `Qt Graphical Effects` QML module
2. Install Roboto font (optional, you can change to other font, see below)
3. `git clone https://github.com/RadRussianRus/sddm-slice.git`
4. `cp -r sddm-slice/slice /usr/share/sddm/themes/slice`
5. Open `/etc/sddm.conf` and put `Current=slice` in `[Theme]` section

## Configuration

Create file `theme.conf.user` in theme folder. See `slice/theme.conf` for reference.

### Base options

* `background` - path to background image. If not set, falls back to `color_bg`. Not set by default.
* `bg_mode` - background image fill mode. Can be either `aspect`, `fill`, `tile` or `none`. Defaults to `aspect`.
* `parallax_bg_shift` - shifting of parallax background on tab change in pixels. `0` disables parallax motion. Negative values will scroll background in opposite direction. Default is `20`.

### Debug mode options

There are some things that can't be tested well in greeter (e.g. shutdown options or login error). So there is a debug mode.

#### Boolean options

> You can use "0/1", "true/false" and "yes/no" on boolean options. All debug options are disabled by default.

* `debug` - activates debug mode.
* `debug_can_power_off` - sets `sddm.canPowerOff` (shows "Shutdown").
* `debug_can_reboot` - sets `sddm.canReboot` (shows "Reboot").
* `debug_can_suspend` - sets `sddm.canSuspend` (shows "Suspend").
* `debug_can_hibernate` - sets `sddm.canHibernate` (shows "Hibernate").
* `debug_can_hybrid_sleep` - sets `sddm.canHybridSleep` (shows "Hybrid Sleep").
* `debug_login_error` - forces login error.


#### Number options

* `debug_login_timeout` - time between pressing "Login" and login error in seconds. Not effective if `debug_login_error` is disabled.

#### String options

* `debug_hostname` - sets `sddm.hostName`.


### Color scheme

There are many color options. In fact, too many. So now they are grouped by layers in [color scheme](https://github.com/RadRussianRus/sddm-slice/wiki/Color-Scheme). Most of them are optional, only mandatory options are from [layer 1](https://github.com/RadRussianRus/sddm-slice/wiki/Color-Scheme-Layer-1):

* `color_bg` - background color. Defaults to `#222222`.
* `color_main` - main color. Defaults to `#dddddd`.
* `color_dimmed` - dimmed main color. Defaults to `#888888`.
* `color_contrast` - color that contrasting to both main and dimmed. Defaults to `#1f1f1f`.

Info about other layers can be found on wiki: [layer 2](https://github.com/RadRussianRus/sddm-slice/wiki/Color-Scheme-Layer-2), [layer 3](https://github.com/RadRussianRus/sddm-slice/wiki/Color-Scheme-Layer-3).

### Font scheme

There are also many font options, so there is now [font scheme](https://github.com/RadRussianRus/sddm-slice/wiki/Font-Scheme) too. Most of them are optional, only mandatory option is from [layer 1](https://github.com/RadRussianRus/sddm-slice/wiki/Font-Scheme-Layer-1):

* `font` - overall font. Defaults to `Roboto`.

Info about other layers can be found on wiki: [layer 2](https://github.com/RadRussianRus/sddm-slice/wiki/Font-Scheme-Layer-2), [layer 3](https://github.com/RadRussianRus/sddm-slice/wiki/Font-Scheme-Layer-3).

## License

Icons: [Material Design Icons](https://github.com/Templarian/MaterialDesign)

[![CC-BY-SA](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)