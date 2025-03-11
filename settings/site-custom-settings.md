# Site custom settings

## SmartCover

<table><thead><tr><th width="233">Code</th><th width="127">Default</th><th>Values</th><th>Description</th></tr></thead><tbody><tr><td>mode</td><td>progressive</td><td>blank<br>header<br>footer<br>banner<br>progressive (default)</td><td>The display mode for the web site</td></tr><tr><td>progressive_autostart</td><td>0</td><td>integer</td><td>Number of seconds before progressive mode automaticaly start displaying.</td></tr><tr><td>progressive_scroll</td><td>200</td><td>integer</td><td>Number of pixel before to display (also number of pixels for scroll up)</td></tr><tr><td>hide_1_min</td><td>0</td><td>integer</td><td>seconds of the start of the first period</td></tr><tr><td>hide_1_max</td><td>5</td><td>integer</td><td>secondes of the end</td></tr><tr><td>hide_1_dist</td><td>1600</td><td>integer</td><td>pixels to scroll to hide</td></tr><tr><td>hide_2_min</td><td>6</td><td>integer</td><td>seconds of the start of the second period</td></tr><tr><td>hide_2_max</td><td>15</td><td>integer</td><td>secondes of the end</td></tr><tr><td>hide_2_dist</td><td>1000</td><td>integer</td><td>pixels to scroll to hide</td></tr><tr><td>hide_3_min</td><td>16</td><td>integer</td><td>seconds of the start of the third period</td></tr><tr><td>hide_3_max</td><td>360</td><td>integer</td><td>secondes of the end</td></tr><tr><td>hide_3_dist</td><td>600</td><td>integer</td><td>pixels to scroll to hide</td></tr><tr><td>close_button</td><td>false</td><td>bool (false / true)</td><td>Add or not a close button on every campagne</td></tr></tbody></table>

```
// Some code
```

## SmartScroll

| Code         | Default | Value             | Description                                                                |
| ------------ | ------- | ----------------- | -------------------------------------------------------------------------- |
| final\_close | false   | bool (false/true) | Enable when the "minimized"  button is clicked to never open the ad again. |

## SmartRead

| Code            | Default | Value             | Description                               |
| --------------- | ------- | ----------------- | ----------------------------------------- |
| disable\_pip    | false   | bool (false/true) | Disable the Picture in Picture experience |
| disable\_vision | false   | bool (false/true) | Disable the Vision experience             |

## SmartSkin

<table><thead><tr><th width="90.96484375">Code</th><th>Label</th><th width="115.27734375">Default</th><th width="133.1328125">Value</th><th>Description</th></tr></thead><tbody><tr><td>sm</td><td>Sticky Mode</td><td>c</td><td>c : class <br>t : transform<br>cs : custom</td><td>Manage the sticky mode by using a specific class "smk_top" or by managing transform on main element.</td></tr><tr><td>tit</td><td>Transform Initial Top</td><td>0</td><td>integer</td><td>Distance in pixels to the top of the website when the scroll is at the top.<br>* Only in transform mode</td></tr><tr><td>tst</td><td>Transform Scrolling Top</td><td>0</td><td>integer</td><td>Distance to keep on top when scrolling.<br>* Only in transform mode</td></tr><tr><td>tee</td><td>Transform Exist Element</td><td></td><td>string</td><td>Query identifier to have alternate initial and scrolling top value if the element is present.<br>* Only in transform mode</td></tr><tr><td>teeit</td><td>Transform Exist Element Initial Top</td><td>0</td><td>integer</td><td>Distance in pixels to the top of the website when the scroll is at the top  and when element is present.<br>* Only in transform mode</td></tr><tr><td>teest</td><td>Transform Exist Element Scrolling Top</td><td>0</td><td>integer</td><td>Distance to keep on top when scrolling and when element is present.<br>* Only in transform mode</td></tr><tr><td>bck</td><td>Background Element</td><td>body</td><td>string</td><td>Query identifier of the element to apply the background color.</td></tr></tbody></table>

You can also have you own custom sticky javascript function :&#x20;

```
smxDeep._window._run_id_scrollCustom = function() {
    //Your own function
}

//Example detecting sub navigation
smxDeep._window._run_id_scrollCustom = function() {
    var subNav = smxDeep._document.querySelector(".sub-nav-wrapper");
    var contentDiv =  smxDeep._document.body;
    var smk =  smxDeep._document.getElementById("_run_id_smk");

    if(subNav != null) {
        var initialTop = 179;
    } else {
        var initialTop = 139;
    }
    var scrollingTop = 40;

    var rect = contentDiv.getBoundingClientRect();

    if(smk != null) {
        smk.style.position = "fixed";
        if( rect.top + parseInt(initialTop) > scrollingTop) {
            smk.style.transform = "translateY(" + ( rect.top + parseInt(initialTop)) + "px)";
        } else {
            smk.style.transform = "translateY("+scrollingTop+"px)";
        }
    }
}
```

