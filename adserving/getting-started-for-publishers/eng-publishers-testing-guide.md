# \[ENG] Publishers : Testing Guide

This guide is designed to help publishers easily test OursBlanc's **specific ad formats** using their ad server, whether it's **Google Ad Manager, Equativ, or Xandr**.

Although OursBlanc formats are **custom and not compatible with standard ad formats**, they can be implemented **quickly and effortlessly** on your site without requiring any technical intervention from your teams. In just a few minutes, you can launch tests, and once the test campaigns are running, our teams will **fully handle the integration and adaptation** of our formats to your site.

## **Pre-requisites Before Testing**

Before providing you with the test scripts, it's important to note that **most of our formats require a "friendly frame" environment**. Depending on your ad server, this might require a **modification when setting up the ad creative**.

🔹 **Google Ad Manager**: Make sure to **uncheck the "Safe Frame" option** to allow our formats to function properly.

Once this setup is complete, our formats can be displayed in **any size**, from the smallest (1x1 pixel) to the largest (e.g., a 1800x1000-pixel skin). Since our formats **extend beyond their placement area**, you can **freely define the best dimensions** for your tagging strategy.

## **Best Practices for Optimal Display**

To ensure smooth delivery and avoid issues, keep the following in mind:

✅ **Avoid calling the same format multiple times on the same page**, as this may cause conflicts—especially when using Google Ad Manager’s "Preview" mode.

✅ **Our formats do not support refresh mechanisms**, which can disrupt their proper display.

✅ **Lazy loading techniques** can also negatively impact their performance.

Aside from these considerations, the **integration process remains the same for all our formats**, including **SmartCover, SmartScroll, SmartRead, SmartPulse, SmartMax, and SmartSkin**.

🚀 **By following these guidelines, you can quickly test and maximize the potential of our formats on your site.**

## Setting Up Campaigns on Google Ad Manager (GAM)

Setting up a test campaign with **Google Ad Manager** is very simple. Overall, the process remains the same as for a **standard display campaign**. The only difference is during the **creative setup**, where you need to select a **custom creative type**.

### Creating the Custom Creative

During the creative setup phase associated with your **Line Item**, you must select the **"Custom"** format.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

When configuring the creative, ensure that you **maintain the ad unit size** you wish to target. As mentioned earlier, our formats can be displayed in **any size**, including **Out of Page** formats.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Next, simply **copy and paste** the script provided by our **SmartXSP platform** (or use the ones available later in this document for testing). **No modifications to the script are required.**

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The **Click-through URL field does not need to be filled in**, as the **click-through URL is managed directly** by our **SmartXSP platform**.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
The most crucial step: **you must uncheck the "Served in a SafeFrame" option**. Without this, **our format will not display on your site**.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Once this step is completed, you can **save your creative** and start seeing your campaign **go live on your site**.

### SmartCover

#### SmartCover image

{% hint style="info" %}
Demo : [https://demo.smartxsp.io/?pvw=xp19Txrx0x7x2177pMf\&pvwc=x02aM9xrxpx1x07p11M9\&format=smc](https://demo.smartxsp.io/?pvw=xp19Txrx0x7x2177pMf\&pvwc=x02aM9xrxpx1x07p11M9\&format=smc)
{% endhint %}

```
<!-- SmartXSP SmartCover Campaign (GAM)
Campaign : #1074 - [Imagine] SmartCover 
Creative:  #1250 - SmartCover - Image - 1250
-->
<script src="https://ng.deepsmx.com/smx.js?id=smx_1074" class="smx_script"></script>
<div id="deepsmx_3b66" class="smx_ph"></div>
<script>
    smxDeep.addKeyValue('gam_width','%%WIDTH%%');
    smxDeep.addKeyValue('gam_height','%%HEIGHT%%');
    smxDeep.addKeyValue('gam_eadv','%eadv!');
    smxDeep.addKeyValue('gam_epid','%epid!');
    smxDeep.addKeyValue('gam_eaid','%eaid!');
    smxDeep.addKeyValue('gam_ecid','%ecid!');
    smxDeep.addKeyValue('gam_ebuy','%ebuy!');
    smxDeep.addKeyValue('gam_cachebuster','%%CACHEBUSTER%%');
    smxDeep.addKeyValue('gam_site','%%SITE%%');

    
    smxDeep._adserver="gam";
    smxDeep.push();

    deepsmx_3b66 = smxDeep.addBlock('deepsmx_3b66',smxDeep._format);
    deepsmx_3b66.setClickTrack('%%CLICK_URL_UNESC%%');
    deepsmx_3b66.setViewTrack('%%VIEW_URL_UNESC%%');
    deepsmx_3b66.setClickTarget('_blank');
    deepsmx_3b66.setCreativeId('1250');
    deepsmx_3b66.push();
</script>
```

#### SmartCover Mini Video

{% hint style="info" %}
Demo : [https://demo.smartxsp.io/?pvw=78Mf1rxrx0x7x22e2c7p\&pvwc=29x719xrxpx9TMx7022\&format=smc](https://demo.smartxsp.io/?pvw=78Mf1rxrx0x7x22e2c7p\&pvwc=29x719xrxpx9TMx7022\&format=smc)
{% endhint %}

```
<!-- SmartXSP SmartCover Campaign (GAM)
Campaign : #1074 - [Imagine] SmartCover 
Creative:  #1293 - Mini-Video - 1293
-->
<script src="https://ng.deepsmx.com/smx.js?id=smx_1074" class="smx_script"></script>
<div id="deepsmx_3425" class="smx_ph"></div>
<script>
    smxDeep.addKeyValue('gam_width','%%WIDTH%%');
    smxDeep.addKeyValue('gam_height','%%HEIGHT%%');
    smxDeep.addKeyValue('gam_eadv','%eadv!');
    smxDeep.addKeyValue('gam_epid','%epid!');
    smxDeep.addKeyValue('gam_eaid','%eaid!');
    smxDeep.addKeyValue('gam_ecid','%ecid!');
    smxDeep.addKeyValue('gam_ebuy','%ebuy!');
    smxDeep.addKeyValue('gam_cachebuster','%%CACHEBUSTER%%');
    smxDeep.addKeyValue('gam_site','%%SITE%%');

    
    smxDeep._adserver="gam";
    smxDeep.push();

    deepsmx_3425 = smxDeep.addBlock('deepsmx_3425',smxDeep._format);
    deepsmx_3425.setClickTrack('%%CLICK_URL_UNESC%%');
    deepsmx_3425.setViewTrack('%%VIEW_URL_UNESC%%');
    deepsmx_3425.setClickTarget('_blank');
    deepsmx_3425.setCreativeId('1293');
    deepsmx_3425.push();
</script>
```

### SmartPulse

#### SmartPulse Image & Terms

{% hint style="info" %}
Demo : [https://demo.smartxsp.io/?pvw=297a18xrxrx2TM2T29\&pvwc=7rMe1Mxrx2xMx0MdxpM7\&format=smp\&smx\_rndr=true](https://demo.smartxsp.io/?pvw=297a18xrxrx2TM2T29\&pvwc=7rMe1Mxrx2xMx0MdxpM7\&format=smp\&smx_rndr=true)
{% endhint %}

```
<!-- SmartXSP SmartPulse Campaign (GAM)
Campaign : #1143 - [Imagine] SmartPulse 
Creative:  #1460 - Image - Ballentine&#039;s avec Conditions - 1460
-->
<script src="https://ng.deepsmx.com/smx.js?id=smx_1143" class="smx_script"></script>
<div id="deepsmx_bce6" class="smx_ph"></div>
<script>
    smxDeep.addKeyValue('gam_width','%%WIDTH%%');
    smxDeep.addKeyValue('gam_height','%%HEIGHT%%');
    smxDeep.addKeyValue('gam_eadv','%eadv!');
    smxDeep.addKeyValue('gam_epid','%epid!');
    smxDeep.addKeyValue('gam_eaid','%eaid!');
    smxDeep.addKeyValue('gam_ecid','%ecid!');
    smxDeep.addKeyValue('gam_ebuy','%ebuy!');
    smxDeep.addKeyValue('gam_cachebuster','%%CACHEBUSTER%%');
    smxDeep.addKeyValue('gam_site','%%SITE%%');

    
    smxDeep._adserver="gam";
    smxDeep.push();

    deepsmx_bce6 = smxDeep.addBlock('deepsmx_bce6',smxDeep._format);
    deepsmx_bce6.setClickTrack('%%CLICK_URL_UNESC%%');
    deepsmx_bce6.setViewTrack('%%VIEW_URL_UNESC%%');
    deepsmx_bce6.setClickTarget('_blank');
    deepsmx_bce6.setCreativeId('1460');
    deepsmx_bce6.push();
</script>
```

### SmartSkin

#### SmartSkin Mini Video

{% hint style="info" %}
Demo : [https://demo.smartxsp.io/?pvw=2r7px7x2Tx2x9Max0Mf\&pvwc=29x278x1x0xpx8x1MpT\&format=smk](https://demo.smartxsp.io/?pvw=2r7px7x2Tx2x9Max0Mf\&pvwc=29x278x1x0xpx8x1MpT\&format=smk)
{% endhint %}

```
<!-- SmartXSP SmartSkin Campaign (GAM)
Campaign : #4349 - [Imagine] - SmartSkin 
Creative:  #5028 - SmartSkin - Mini Vidéo EVIAN - 5028
-->
<script src="https://ng.deepsmx.com/smx.js?id=smx_4349" class="smx_script"></script>
<div id="deepsmx_fc4d" class="smx_ph"></div>
<script>
    smxDeep.addKeyValue('gam_width','%%WIDTH%%');
    smxDeep.addKeyValue('gam_height','%%HEIGHT%%');
    smxDeep.addKeyValue('gam_eadv','%eadv!');
    smxDeep.addKeyValue('gam_epid','%epid!');
    smxDeep.addKeyValue('gam_eaid','%eaid!');
    smxDeep.addKeyValue('gam_ecid','%ecid!');
    smxDeep.addKeyValue('gam_ebuy','%ebuy!');
    smxDeep.addKeyValue('gam_cachebuster','%%CACHEBUSTER%%');
    smxDeep.addKeyValue('gam_site','%%SITE%%');

    
    smxDeep._adserver="gam";
    smxDeep.push();

    deepsmx_fc4d = smxDeep.addBlock('deepsmx_fc4d',smxDeep._format);
    deepsmx_fc4d.setClickTrack('%%CLICK_URL_UNESC%%');
    deepsmx_fc4d.setViewTrack('%%VIEW_URL_UNESC%%');
    deepsmx_fc4d.setClickTarget('_blank');
    deepsmx_fc4d.setCreativeId('5028');
    deepsmx_fc4d.push();
</script>
```

### SmartRead

#### SmartRead Slider Square & Picture in Picture

{% hint style="info" %}
Demo : [https://demo.smartxsp.io/?pvw=1M797Mx9xpxMxpM718\&pvwc=M72bMax1x2xMx97r291p\&format=smr](https://demo.smartxsp.io/?pvw=1M797Mx9xpxMxpM718\&pvwc=M72bMax1x2xMx97r291p\&format=smr)
{% endhint %}

```
<!-- SmartXSP SmartRead Campaign (GAM)
Campaign : #926 - [Imagine] SmartRead 
Creative:  #5469 - Fluid Slider Square mode - 5469
-->
<script src="https://ng.deepsmx.com/smx.js?id=smx_926" class="smx_script"></script>
<div id="deepsmx_7221" class="smx_ph"></div>
<script>
    smxDeep.addKeyValue('gam_width','%%WIDTH%%');
    smxDeep.addKeyValue('gam_height','%%HEIGHT%%');
    smxDeep.addKeyValue('gam_eadv','%eadv!');
    smxDeep.addKeyValue('gam_epid','%epid!');
    smxDeep.addKeyValue('gam_eaid','%eaid!');
    smxDeep.addKeyValue('gam_ecid','%ecid!');
    smxDeep.addKeyValue('gam_ebuy','%ebuy!');
    smxDeep.addKeyValue('gam_cachebuster','%%CACHEBUSTER%%');
    smxDeep.addKeyValue('gam_site','%%SITE%%');

    
    smxDeep._adserver="gam";
    smxDeep.push();

    deepsmx_7221 = smxDeep.addBlock('deepsmx_7221',smxDeep._format);
    deepsmx_7221.setClickTrack('%%CLICK_URL_UNESC%%');
    deepsmx_7221.setViewTrack('%%VIEW_URL_UNESC%%');
    deepsmx_7221.setClickTarget('_blank');
    deepsmx_7221.setCreativeId('5469');
    deepsmx_7221.push();
</script>
```
