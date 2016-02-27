# HJKL Karabiner Media Keys for OSX

I use a happy hacking keyboard and vim a lot.

Since there is no dedicated media key on my keyboard, I started using Karabiner.

I finally got around to looking through Karabiner docs and created HJKL key bindings for the media keys, enjoy!

## How To Install

1. Install [Karabiner](https://pqrs.org/osx/karabiner/)
2. Edit your private.xml file, typically located at /Users/your_user_name/Library/Application Support/Karabiner/private.xml
3. Copy the private.xml file in this repo or just the parts you need
4. Open up Karabiner and go to the Change Key tab. Reload XML & Select VIM Style Media Keys!
4. If you found this repo helpful, star it!
5. Feel free to open issues for suggestions if you'd like me to add more or want to contribute, thanks!

## The Key Bindings
1. (Option + H) Play Previous
1. (Option + J) Volume Down
1. (Option + K) Volume Up
1. (Option + L) Play Next

## I don't like your modifier key, how can I change it to suit my needs?
Let's take a look at one of the key binding definitions:

```xml
<item>
  <name>VIM Style Volume Down Mapping</name>
  <appendix>Remaps Left OPTION + J to Media Key Volume Down</appendix>
  <identifier>private-music-remap-volume-down</identifier>
  <autogen>
    __KeyToKey__
    KeyCode::J, ModifierFlag::OPTION_L | ModifierFlag::NONE,
    ConsumerKeyCode::VOLUME_DOWN
  </autogen>
</item>
```

Just change ``` ModifierFlag::OPTION_L ``` to any of these:

- ModifierFlag::ZERO
- ModifierFlag::CAPSLOCK
- ModifierFlag::SHIFT_L
- ModifierFlag::SHIFT_R
- ModifierFlag::CONTROL_L
- ModifierFlag::CONTROL_R
- ModifierFlag::OPTION_L
- ModifierFlag::OPTION_R
- ModifierFlag::COMMAND_L
- ModifierFlag::COMMAND_R
- ModifierFlag::NUMPAD
- ModifierFlag::FN
- ModifierFlag::NONE

## Need more help?

Open an issue and I'll help you out.
