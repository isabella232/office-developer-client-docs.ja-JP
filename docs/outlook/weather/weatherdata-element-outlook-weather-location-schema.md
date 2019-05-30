---
title: weatherdata 要素 (Outlook Weather Location スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: 天気予報の要素を定義します。
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540932"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="608cd-103">weatherdata 要素 (Outlook Weather Location スキーマ)</span><span class="sxs-lookup"><span data-stu-id="608cd-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="608cd-104">天気予報の要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="608cd-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="608cd-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="608cd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="608cd-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="608cd-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="608cd-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="608cd-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="608cd-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="608cd-108">**Schema file**</span></span> <br/> |<span data-ttu-id="608cd-109">getweatherlocation</span><span class="sxs-lookup"><span data-stu-id="608cd-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="608cd-110">定義</span><span class="sxs-lookup"><span data-stu-id="608cd-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="608cd-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="608cd-111">Elements and attributes</span></span>

<span data-ttu-id="608cd-112">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="608cd-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="608cd-113">親要素</span><span class="sxs-lookup"><span data-stu-id="608cd-113">Parent elements</span></span>

<span data-ttu-id="608cd-114">なし。</span><span class="sxs-lookup"><span data-stu-id="608cd-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="608cd-115">子要素</span><span class="sxs-lookup"><span data-stu-id="608cd-115">Child elements</span></span>

|<span data-ttu-id="608cd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="608cd-116">**Element**</span></span>|<span data-ttu-id="608cd-117">**型**</span><span class="sxs-lookup"><span data-stu-id="608cd-117">**Type**</span></span>|<span data-ttu-id="608cd-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="608cd-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="608cd-119">天気予報</span><span class="sxs-lookup"><span data-stu-id="608cd-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="608cd-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="608cd-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="608cd-121">気象を報告する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="608cd-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="608cd-122">属性</span><span class="sxs-lookup"><span data-stu-id="608cd-122">Attributes</span></span>

<span data-ttu-id="608cd-123">なし。</span><span class="sxs-lookup"><span data-stu-id="608cd-123">None.</span></span>
  

