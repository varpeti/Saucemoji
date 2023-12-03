# Saucemoji
Know-how to configure fallback from SauceCodePro NF to Noto Color Emoji

## Prerequisites
- Install fonts (on Arch): `sudo pacman -Suy ttf-sourcecodepro-nerd noto-fonts-emoji`
- Reload font cache: `fc-cache`

## FontConfig
Add the following lines to your font config: (~/.config/fontconfig/fonts.conf)
```xml
<fontconfig>
...


<!--
  Custom fallback
-->
  <alias>
   <family>Saucemoji</family>
   <prefer>
     <family>SauceCodePro NF</family>
     <family>Noto Color Emoji</family>
   </prefer>
  </alias>


...
</fontconfig>
```

## Set the `Saucemoji` as the font in any app or in the system
Left as an exercise for the reader 🙈
