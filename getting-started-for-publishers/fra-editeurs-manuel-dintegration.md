---
description: Manuel d'intégration des Formats Spécifiques OursBlanc pour les éditeurs.
---

# \[FRA] - Editeurs : Manuel d'intégration

Ce guide a pour objectif de permettre aux éditeurs de tester facilement les formats spécifiques d’OursBlanc à l’aide de leur ad serveur, qu’il s’agisse de **Google Ad Manager, Equativ ou Xandr**.

Bien que les formats OursBlanc soient **spécifiques et non compatibles avec les standards classiques**, leur diffusion sur votre site reste très simple et ne nécessite aucune intervention de vos équipes techniques. En seulement quelques minutes, vous pouvez les intégrer et tester leur fonctionnement. Une fois les campagnes de test en cours de diffusion, nos équipes prendront en charge **l’intégration et l’adaptation** des formats à votre site.

## Pré-requis avant le lancement des tests

Avant de vous fournir les scripts de test, il est important de noter que **la plupart de nos formats nécessitent un environnement "friendly frame"**. Selon l’ad serveur utilisé, il peut être nécessaire d’apporter une **modification lors de la création du visuel**.

🔹 **Google Ad Manager** : pensez à **décocher la case "Safe Frame"** pour assurer le bon fonctionnement de nos formats.

Une fois cette configuration réalisée, nos formats peuvent être diffusés dans **toutes les tailles**, de la plus petite (1x1 pixel) à la plus grande (ex. : habillage de 1800x1000 pixels). Nos formats ne sont **pas limités** par leur zone d’emplacement, ce qui vous permet d’adapter leur dimension en fonction de votre stratégie de taggage.

## Bonnes pratiques pour une diffusion optimale

Pour garantir une diffusion fluide et éviter tout dysfonctionnement, voici quelques points de vigilance :

✅ **Évitez d’appeler un même format plusieurs fois sur une même page**, notamment lors de l’utilisation du mode "Preview" de Google Ad Manager, qui peut générer des conflits.

✅ **Nos formats ne supportent pas les mécanismes de refresh**, qui peuvent perturber leur affichage.

✅ **Les techniques de lazy loading** peuvent également avoir un impact négatif sur leur bonne diffusion.

Hormis ces précautions, la procédure d’intégration reste **identique pour tous nos formats**, qu’il s’agisse du **SmartCover, SmartScroll, SmartRead, SmartPulse, SmartMax ou SmartSkin**.

🚀 **En suivant ces recommandations, vous pourrez tester et exploiter pleinement la puissance de nos formats sur votre site.**

## **Mise en place des campagnes sur Google Ad Manager (GAM)**

La mise en place d’une campagne de test avec **Google Ad Manager** est très simple. Dans l’ensemble, le processus reste identique à celui d’une **campagne display classique**. La seule différence intervient **lors de la création du visuel**, où vous devrez sélectionner un **visuel de type personnalisé**.

### **Création du visuel personnalisé**

Lors de la phase de création du visuel associé à votre Line Item, vous devez choisir le format "Personnalisée" :&#x20;

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Sélection du type de visuel Personnalisé</p></figcaption></figure>

Lors de la création proprement dite, vous devez conserver la **taille du bloc d'annonces** que vous souhaitez cibler. Comme mentionné précédemment, nos formats peuvent être diffusés **dans toutes les tailles**, y compris sur les formats **hors page (Out of Page)**.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Il vous suffit ensuite de **copier/coller le script fourni par notre plateforme SmartXSP** (ou d’utiliser ceux disponibles dans la suite de ce document pour vos tests). **Aucune modification du script n’est nécessaire.**

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

La zone **URL de destination** n’a pas besoin d’être remplie. En effet, l’**URL utilisée lors du clic sur la publicité est gérée directement** par notre plateforme **SmartXSP**.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Enfin, l’élément le plus important : **il est impératif de décocher la case "Diffusée dans un cadre SafeFrame"**. Sans cette action, **notre format ne pourra pas s’afficher sur votre site.**
{% endhint %}

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>Case à décocher impérativement.</p></figcaption></figure>

Une fois cette étape terminée, vous pouvez **enregistrer votre visuel** et commencer à voir votre campagne **se diffuser** sur votre site.

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

