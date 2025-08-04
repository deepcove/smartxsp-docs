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
| container       | empty   | QuerySelector     | Set the element to display the SmartRead  |

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

## SmartView

<table><thead><tr><th width="92.0078125">Code</th><th width="109.8125">Default</th><th width="149.046875">Value</th><th>Description</th></tr></thead><tbody><tr><td>v</td><td>empty</td><td>original</td><td>Switch to original display mode</td></tr><tr><td>header</td><td>empty</td><td>QuerySelector</td><td>Auto position under this element </td></tr><tr><td>menu</td><td>empty</td><td>QuerySelector</td><td><strong>Element below the menu</strong> that can be visible or not, independently of the header. It can only exist if a header is defined. The SmartView will be placed below the lowest element between the header and the menu. The menu can be a collection of elements.</td></tr><tr><td>content</td><td>empty</td><td>QuerySelector</td><td><strong>The site content must be shifted downward.</strong> The content will appear just below the SmartView.</td></tr><tr><td>mode</td><td>scroll</td><td>scroll<br>class</td><td>Indicates how to adjust the SmartView’s height to position it below an element.</td></tr><tr><td>element</td><td>empty</td><td>QuerySelector</td><td><strong>Scroll</strong> will adjust the height based on scrolling, while <strong>class</strong> will adjust it when the class changes.</td></tr><tr><td>scrm</td><td>600</td><td>Integer</td><td>Distance in pixel to minimize</td></tr><tr><td>class</td><td>empty</td><td>String</td><td>Requires the <strong>Key|Value</strong> pair: <code>mode|class</code>. Allows targeting the element whose class changes to hide/show it.</td></tr><tr><td>scr1</td><td>3000</td><td>Integer</td><td>Distance in pixel to disappear on interval t1 > t2</td></tr><tr><td>scr2</td><td>2000</td><td>Integer</td><td>Distance in pixel to disappear on interval t2 > t3</td></tr><tr><td>scr3</td><td>1000</td><td>Integer</td><td>Distance in pixel to disappear on interval t3 ></td></tr><tr><td>tps1</td><td>4</td><td>Integer</td><td>Sanctuarisation of the expand mode (in seconds)</td></tr><tr><td>tps2</td><td>15</td><td>Integer</td><td>End time of high scroller user (between tps1 and tps2)</td></tr><tr><td>tps3</td><td>40</td><td>Integer</td><td>End time of medium scroller user (between tps2 and tps3)</td></tr><tr><td>tpsc</td><td>180</td><td>Integer</td><td>End time of low scroller user and time to auto disappear of the ad</td></tr></tbody></table>

