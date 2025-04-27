# 🌲 Earthshaker Sway Theme

**Earthshaker** is a full SwayWM theme designed to bring the living forest to your Linux desktop.

Built from the Earthshaker aesthetic — warm earth tones, lively greens, wildflower highlights, and deep forest shadows — this theme is meant to feel grounded, alive, and familiar without being overly bright or distracting.

Originally crafted for the personal system of *Remus Alexander* as part of a larger narrative, Earthshaker is now available for anyone seeking to build a calm, breathing environment in their workspace.

---

## 📦 Features

- Full color palette inspired by living forests 🌳
- Customized window (`client.*`) styling
- Fully themed Swaybar: focused, active, inactive, urgent workspaces
- Seamless palette integration with Neovim Earthshaker and terminal environments
- Soft, living contrast — bright where needed, muted elsewhere

---

## 🎨 Palette Overview

| Name         | Color    | Description                  |
|--------------|----------|-------------------------------|
| Forest Floor | `#1a1c1b` | Main background base          |
| Sunlight     | `#e0d6c3` | Text and soft highlights      |
| Wildflower   | `#ffc07c` | Focus indicators              |
| Berrythorn   | `#ff6655` | Urgent signals                |
| Sage         | `#6c8f6c` | Focused workspace highlight   |
| Barkdark     | `#2c302c` | Secondary background surfaces |
| Lightsage    | `#c9d8b6` | Inactive text                 |

*(Full variable mappings available inside the theme files.)*

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/remusalexander/earthshaker.sway.git ~/.config/sway/themes/earthshaker
```

Then in your Sway config:

```bash
include ~/.config/sway/themes/earthshaker/earthshaker
```

---

## Reference in config

You can setup your config to look like this

```
# target                   title         bg             text         indicator    border
client.focused            $sunlight      $forestfloor   $wildflower  $berrythorn  $sunlight
client.focused_inactive   $overlay_barkshadow $forestfloor $lightsage $berrythorn $overlay_barkshadow
client.unfocused          $overlay_barkshadow $forestfloor $lightsage $berrythorn $overlay_barkshadow
client.urgent             $pollen        $forestfloor   $pollen      $overlay_barkshadow $pollen
client.placeholder        $overlay_barkshadow $forestfloor $lightsage $overlay_barkshadow $overlay_barkshadow
client.background         $forestfloor

```

and for your Swaybar

```
        colors {
            background          $forestfloor
            statusline          $sunlight
            focused_statusline  $sunlight
            focused_separator   $forestfloor

            #target             border          bg                text
            focused_workspace   $forestfloor    $sage             $blacksoil
            active_workspace    $forestfloor    $barkdark         $sunlight
            inactive_workspace  $forestfloor    $forestfloor      $lightsage
            urgent_workspace    $forestfloor    $berrythorn       $blacksoil
        }

```
