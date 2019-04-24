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
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355035"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="d67ec-103">weatherdata 要素 (Outlook Weather Location スキーマ)</span><span class="sxs-lookup"><span data-stu-id="d67ec-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="d67ec-104">天気予報の要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="d67ec-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d67ec-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d67ec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d67ec-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d67ec-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="d67ec-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d67ec-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="d67ec-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d67ec-108">**Schema file**</span></span> <br/> |<span data-ttu-id="d67ec-109">getweatherlocation</span><span class="sxs-lookup"><span data-stu-id="d67ec-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d67ec-110">定義</span><span class="sxs-lookup"><span data-stu-id="d67ec-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d67ec-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d67ec-111">Elements and attributes</span></span>

<span data-ttu-id="d67ec-112">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d67ec-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d67ec-113">親要素</span><span class="sxs-lookup"><span data-stu-id="d67ec-113">Parent elements</span></span>

<span data-ttu-id="d67ec-114">なし。</span><span class="sxs-lookup"><span data-stu-id="d67ec-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d67ec-115">子要素</span><span class="sxs-lookup"><span data-stu-id="d67ec-115">Child elements</span></span>

|<span data-ttu-id="d67ec-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d67ec-116">**Element**</span></span>|<span data-ttu-id="d67ec-117">**型**</span><span class="sxs-lookup"><span data-stu-id="d67ec-117">**Type**</span></span>|<span data-ttu-id="d67ec-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="d67ec-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d67ec-119">天気予報</span><span class="sxs-lookup"><span data-stu-id="d67ec-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="d67ec-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="d67ec-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="d67ec-121">気象を報告する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="d67ec-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d67ec-122">属性</span><span class="sxs-lookup"><span data-stu-id="d67ec-122">Attributes</span></span>

<span data-ttu-id="d67ec-123">なし。</span><span class="sxs-lookup"><span data-stu-id="d67ec-123">None.</span></span>
  

