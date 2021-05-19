---
title: weatherdata 要素 (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: weather 要素を定義します。
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538985"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="8adef-103">weatherdata 要素 (Outlook天気予報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="8adef-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="8adef-104">weather 要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="8adef-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8adef-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="8adef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8adef-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8adef-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="8adef-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8adef-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="8adef-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8adef-108">**Schema file**</span></span> <br/> |<span data-ttu-id="8adef-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="8adef-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8adef-110">定義</span><span class="sxs-lookup"><span data-stu-id="8adef-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8adef-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8adef-111">Elements and attributes</span></span>

<span data-ttu-id="8adef-112">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8adef-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8adef-113">親要素</span><span class="sxs-lookup"><span data-stu-id="8adef-113">Parent elements</span></span>

<span data-ttu-id="8adef-114">なし。</span><span class="sxs-lookup"><span data-stu-id="8adef-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8adef-115">子要素</span><span class="sxs-lookup"><span data-stu-id="8adef-115">Child elements</span></span>

|<span data-ttu-id="8adef-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8adef-116">**Element**</span></span>|<span data-ttu-id="8adef-117">**型**</span><span class="sxs-lookup"><span data-stu-id="8adef-117">**Type**</span></span>|<span data-ttu-id="8adef-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="8adef-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8adef-119">天気</span><span class="sxs-lookup"><span data-stu-id="8adef-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="8adef-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="8adef-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="8adef-121">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="8adef-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8adef-122">属性</span><span class="sxs-lookup"><span data-stu-id="8adef-122">Attributes</span></span>

<span data-ttu-id="8adef-123">なし。</span><span class="sxs-lookup"><span data-stu-id="8adef-123">None.</span></span>
  

