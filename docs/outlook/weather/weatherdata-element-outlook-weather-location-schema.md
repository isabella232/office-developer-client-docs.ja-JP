---
title: weatherdata 要素 (Outlook場所スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: weather 要素を定義します。
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540932"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="8007a-103">weatherdata 要素 (Outlook場所スキーマ)</span><span class="sxs-lookup"><span data-stu-id="8007a-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="8007a-104">weather 要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="8007a-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8007a-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="8007a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8007a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8007a-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="8007a-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8007a-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="8007a-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8007a-108">**Schema file**</span></span> <br/> |<span data-ttu-id="8007a-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="8007a-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8007a-110">定義</span><span class="sxs-lookup"><span data-stu-id="8007a-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8007a-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8007a-111">Elements and attributes</span></span>

<span data-ttu-id="8007a-112">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8007a-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8007a-113">親要素</span><span class="sxs-lookup"><span data-stu-id="8007a-113">Parent elements</span></span>

<span data-ttu-id="8007a-114">なし。</span><span class="sxs-lookup"><span data-stu-id="8007a-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8007a-115">子要素</span><span class="sxs-lookup"><span data-stu-id="8007a-115">Child elements</span></span>

|<span data-ttu-id="8007a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8007a-116">**Element**</span></span>|<span data-ttu-id="8007a-117">**型**</span><span class="sxs-lookup"><span data-stu-id="8007a-117">**Type**</span></span>|<span data-ttu-id="8007a-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="8007a-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8007a-119">天気</span><span class="sxs-lookup"><span data-stu-id="8007a-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="8007a-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="8007a-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="8007a-121">天気予報を報告する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="8007a-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8007a-122">属性</span><span class="sxs-lookup"><span data-stu-id="8007a-122">Attributes</span></span>

<span data-ttu-id="8007a-123">なし。</span><span class="sxs-lookup"><span data-stu-id="8007a-123">None.</span></span>
  

