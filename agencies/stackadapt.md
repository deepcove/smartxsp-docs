# StackAdapt

Welcome to our guide on effectively utilizing our ad formats within the StackAdapt DSP. In this documentation, we will walk you through the process of activating private deals to ensure high visibility rates—around 70%—of your creatives. Additionally, we'll cover how to create and implement the visual components of your campaigns, pulling scripts from the SmartXSP platform and ensuring everything is validated and ready to go.

## **Activating Private Deals on StackAdapt**

The first step in adding a deal on StackAdapt is to ensure that you have access to the "BYOD" (Build Your Own Deal) feature. If your agency doesn't yet have this functionality enabled, you'll need to request its activation from your StackAdapt representative.

<figure><img src="../.gitbook/assets/image (13).png" alt="" width="248"><figcaption></figcaption></figure>

Once you have access, log into StackAdapt and navigate to the "Inventory" menu. Under this menu, you'll find a sub-menu called "My Inventory." This is where you can access the list of inventories available to you. If the BYOD feature is activated, you'll see a dedicated BYOD tab. Clicking on this tab will open a new section where you can create your own deals.

<figure><img src="../.gitbook/assets/image (15).png" alt="" width="322"><figcaption></figcaption></figure>

In the top right corner of the BYOD page, you'll find a button that allows you to create a new deal. You have the option to choose between a Programmatic Guaranteed (PG) deal or a Private Marketplace (PMP) deal. For our purposes, we will select the Private Marketplace option. This will open a form that you'll need to fill out in order to create your deals.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Currently, we recommend creating two separate deals: one for mobile devices and one for desktop devices. We'll include screenshots to illustrate exactly how to fill out the form for each type of deal.&#x20;

### Deal for mobile devices

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### Deal for desktop devices

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Additionally, we provide a summary table highlighting the key information you need to record, particularly the Deal ID that is generated in the system.

<table><thead><tr><th width="149.18359375">Deal ID</th><th width="84.37109375">Channel</th><th width="197.94921875">SSP</th><th width="204.6875">Publisher Name</th><th>Device</th></tr></thead><tbody><tr><td>955542578031</td><td>Display</td><td>Equativ (Display/In-Ad)</td><td>Agence Ours Blanc - FR</td><td>Mobile</td></tr><tr><td>187391524564</td><td>Display</td><td>Equativ (Display/In-Ad)</td><td>Agence Ours Blanc - FR</td><td>Desktop</td></tr></tbody></table>

## **Part 2: Creating the Campaign and Integrating the Creative Code**

To start, you will create your campaign within our SmartXSP platform. Simply navigate to the "Campaign" menu and select the option to create a new campaign. Make sure that the "Ad Server" buying strategy is selected. Once your campaign is set up, and you've created your creative as you normally would, the next step is to retrieve the code that you'll need to implement in StackAdapt.

To do this, go to the campaign details in SmartXSP and navigate to the "**Managed**" tab. Within this tab, you'll be able to select the appropriate ad server from a dropdown list—in this case, you'll choose **StackAdapt**. Once selected, the platform will automatically generate the code you need. You can then use the "Copy to Clipboard" function to easily grab this code.

In StackAdapt, you'll create your campaign just as you normally would. The key difference when using our OursBlanc premium formats is that you'll need to select the private deals you previously created. You can choose the mobile deal, the desktop deal, or both, depending on the needs of your campaign.&#x20;

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

To do this, head over to the "Inventory" section in StackAdapt, and select “Edit Inventory.” Under the “BYOD-PMP” tab, you’ll find the deals you set up earlier—like the OursBlanc premium mobile and desktop formats. This is the first unique step when setting up SmartXSP OursBlanc formats.

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
We recommend you to check "Run only on theses Inventory Packages/PMP Deals" to ensure the correct delivery.
{% endhint %}

The second unique step comes when you're adding the creative. Click on “Add New” to create a new creative, and instead of uploading an image, you’ll choose the “3rd Party Tag” option.&#x20;

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

At this point, you’ll need to select a size for your creative. To maximize reach, it’s recommended to create multiple versions of the creative using the same script but in different sizes. The primary sizes we recommend are 300x250 and 320x50. You can also include additional sizes like 320x100, 300x600, or 768x90 for even more reach.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Once you’ve pasted the code you copied from SmartXSP and filled out the remaining fields, your setup is complete. With these steps done, your campaign is ready to deliver the unique OursBlanc formats.



