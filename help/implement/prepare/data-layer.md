---
title: Create a data layer
description: Learn what a data layer is in your Analytics implementation, and how it can be used to map variables in Adobe Analytics.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
role: Admin, Developer, Leader
---
# Create a data layer

* data layer
  * 💡:= framework of JavaScript objects | your site 💡/
    * contain the variable values -- used -- | YOUR Analytics implementation
    * allows
      * | assigning values | Analytics variables
        * greater control
        * easier maintenance 
    * extensible
      * == if you have organization's requirements specific -> include objects | your data layer

## Prerequisites

* [Create a solution design document](solution-design.md) 
  * == align on tracking requirements

## Steps

1. implement a data layer 
   1. site development team's responsibility
      1. data layer object -- is populated with -- correct values 
   2. Review this page with your site development team to make sure expectations are aligned between teams.
2. validate your data layer 
   1. -- via -- browser's developer console 
      1. _Example:_ `adobeDataLayer.page.title`
3. map data layer objects -- , via Adobe Experience Platform Data Collection, to -- data elements
   1. based on your organization's implementation method
      1. if you use Web SDK
         1. map the desired data layer objects -- to the -- Adobe Experience Platform Edge's desired XDM fields  
         2. see [Analytics XDM variable mapping](../aep-edge/xdm-var-mapping.md)
      2. if you use the Analytics extension
         1. create data elements /
            1. under Tags | Adobe Experience Platform Data Collection
            2. -- assign them to the -- desired data layer objects
         2. | Analytics extension, assign EACH data element -- to the -- appropriate Analytics variable

## Specifications

* recommendations
  * use [Adobe Client Data Layer](https://github.com/adobe/adobe-client-data-layer/wiki)
    * ALTERNATIVES to Adobe Client Data Layer
      * [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf),

## Setting data layer values

* Data layers
  * -- typically generate -- server-side / 
    * objects referenced == objects -- used to build the -- site content
* site's data layer -- MUST be established, based on -- tracking requirements / set | your organization's [solution design document](solution-design.md)

## Next steps

* [Map data layer objects | data elements](../launch/layer-to-elements.md)
