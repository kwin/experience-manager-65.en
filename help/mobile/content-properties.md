---
title: Content Properties and Nodes
seo-title: Content Properties and Nodes
description: Follow this page to learn about content properties and nodes.
seo-description: Follow this page to learn about content properties and nodes.
uuid: 2dad52c8-5b6c-4b90-8498-62217a9a27fc
contentOwner: User
content-type: reference
products: SG_EXPERIENCEMANAGER/6.5/MOBILE
topic-tags: developing-on-demand-services-app
discoiquuid: f5721ddc-df5c-496c-be61-38d1cab63ad4
exl-id: 05c8c846-69cc-4075-9149-33890b3d1e08
---
# Content Properties and Nodes {#content-properties-and-nodes}

>[!NOTE]
>
>Adobe recommends using the SPA Editor for projects that require single page application framework-based client-side rendering (for example, React). [Learn more](/help/sites-developing/spa-overview.md).

Articles, Banners, and Collections are represented as cq:Pages in AEM.

They share the same common properties found in any cq:Page in addition to several others shown below that represent Adobe Experience Manager (AEM) Mobile On-Demand services metadata and integration supporting properties.

The following tables describe the content properties and nodes.

## Common Integration Properties {#common-integration-properties}

| **Property Name** |**Type** |**Defaults or Expected Values** |**Description** |
|---|---|---|---|
| dps-id |String |  |assigned by AEM Mobile and stored by AEM once uploaded to AEM Mobile or imported from AEM Mobile |
| dps-resourceType |String |dps:Article | dps:Banner | dps:Collection |entity type property |
| dps-version |String |  |version of AEM Mobile entity (also contained within the full aemm-id) |
| dps-lastSynced |Date |  |date of last sync/import from AEM Mobile into AEM |
| dps-lastUploaded |Date |  |date of last upload from AEM to AEM Mobile |
| dps-lastUploadedBy |String:userid |  |id user that performed the last upload request from AEM to AEM Mobile |

## Core Metadata Properties {#core-metadata-properties}

|Property Name|Type|Defaults or Expected Values|
|--- |--- |--- |
|dps-title|String||
|dps-shortTitle|String||
|dps-abstract|String||
|dps-shortAbstract|String||
|dps-department|String||
|dps-category|String||
|dps-keywords|String[]||
|dps-internalKeywords|String[]||
|dps-importance|String[]|Importance from {"low", "normal", "high"}|

### Articles {#articles}

| **Property Name** |**Type** |**Defaults or Expected Values** |
|---|---|---|
| dps-author |String |  |
| dps-authorURL |String |  |
| dps-hideFromBrowsePage |Boolean |  |
| dps-access |String |ProtectedAccess from {"protected", "metered", "free"} |
| **Social** |  |  |
| dps-socialShareURL |String |  |
| dps-articleText |String |  |
| dps-url |String |  |

### Banners {#banners}

| **Property Name** |**Type** |**Defaults or Expected Values** |
|---|---|---|
| dps-tapAction |  |TapAction from {webLink} |
| dps-tapActinUrl |  |  |

### Collections {#collections}

|Property Name|Type|Defaults or Expected Values|
|--- |--- |--- |
|dps-productId|String||
|dps-readingPosition|String|from {"reset","retain"}|
|dps-horizontalSwipe|Boolean||
|dps-allowDownload|Boolean||
|dps-openDefault|String|from {"browsePage","contentView"}|
|dps-layout|String||

## Content Nodes {#content-nodes}

### Common Nodes {#common-nodes}

|Node Name|Type|Defaults or Expected Values|Description|
|--- |--- |--- |--- |
|image|jcr:primaryType=nt:unstructured <br> sling:resourceType=foundation/components/image|||

### Entities {#entities}

#### Articles {#articles-1}

|Node Name|Type|Defaults of Expected Values|Description|
|--- |--- |--- |--- |
|social-share-image||jcr:primaryType=nt:unstructured <br> sling:resourceType=foundation/components/image||

#### Banners {#banners-1}

| Node Name |Type |Defaults of Expected Values |Description |
|---|---|---|---|
|  NA |  |  |  |

#### Collections {#collections-1}

|Node Name|Type|Defaults of Expected Values|Description|
|--- |--- |--- |--- |
|background-image|jcr:primaryType=nt:unstructured <br> sling:resourceType=foundation/components/image|||
