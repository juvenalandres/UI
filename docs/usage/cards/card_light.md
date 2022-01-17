---
title: card_light
---
<!-- markdownlint-disable MD046 -->

## Description

![Image title](../../assets/img/card_light.png){ width="500" }
![Image title](../../assets/img/card_light_slider.png){ width="500" }
![Image title](../../assets/img/card_light_slider_horizontal.png){ width="500" }
![Image title](../../assets/img/card_light_slider_collapse.png){ width="500" }

This documentation refers to the new "All in one" light card.
This card merges the following one :

- legacy `card_light` (the old one)
- legacy `card_light_slider`
- legacy `card_light_slider_collapse`
- legacy `card_light_slider_horizontal`
- custom `card_light_color` by basbruss
- custom `card_light_horizontal_color` by basbruss
- custom `card_light_slider_color` by basbruss
- custom `card_light_slider_collapse_color` by basbruss

!!! warning
    This card has backward compatibilty with older template except custom names and icons. It means variables like `ulm_card_XXX_name` and `ulm_card_XXX_icon` must be replaced by `ulm_card_light_name` and `ulm_card_light_icon`.

## Variables

| Variable/Entity                        | Default         | Required         | Notes          | Requirement |
|----------------------------------------|-----------------|------------------|----------------|-------------|
| entity                                 |                 | :material-check: | Your HA entity |             |
| ulm_card_light_name                    | `friendly_name` | :material-close: | Customize name |             |
| ulm_card_light_icon                    | `mdi:lightbulb` | :material-close: | Customize icon |             |
| ulm_card_light_enable_slider           | `false`         | :material-close: | Enable slider  |             |
| ulm_card_light_enable_collapse         | `false`         | :material-close: | Collapse slider when off | Need `ulm_card_light_enable_slider: true` |
| ulm_card_light_enable_horizontal       | `false`         | :material-close: | Enable horizontal card | |
| ulm_card_light_enable_horizontal_wide  | `false`         | :material-close: | Wider slider | Need `ulm_card_light_enable_horizontal: true` |
| ulm_card_light_enable_color            | `false`         | :material-close: | Enable icon and label light color | |
| ulm_card_light_enable_background_color | `false`         | :material-close: | Enable background light color in dark theme| |
| ulm_card_light_force_background_color  | `false`         | :material-close: | Force background light color even in light theme | Need `ulm_card_light_enable_background_color: true` |

## Usage

```yaml
- type: "custom:button-card"
  template: card_light
  entity: light.allee
  variables:
    ulm_card_light_slider_aio_enable_slider: true
    ulm_card_light_slider_aio_enable_background_color: true
    ulm_card_light_slider_aio_force_background_color: true
```

??? note "Template Code"

    ```yaml title="card_light.yaml"
    --8<-- "custom_components/ui_lovelace_minimalist/lovelace/ulm_templates/card_templates/cards/card_light.yaml"
    ```