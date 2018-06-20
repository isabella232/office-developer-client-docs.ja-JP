---
title: weatherdata 要素 (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: 気象要素を定義します。
ms.openlocfilehash: 689c390f621d18f680de9635c3d82711300f8030
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804576"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="fcb41-103">weatherdata 要素 (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="fcb41-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="fcb41-104">気象要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="fcb41-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fcb41-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="fcb41-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcb41-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="fcb41-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="fcb41-107">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="fcb41-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="fcb41-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fcb41-108">**Schema file**</span></span> <br/> |<span data-ttu-id="fcb41-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="fcb41-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fcb41-110">定義</span><span class="sxs-lookup"><span data-stu-id="fcb41-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fcb41-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fcb41-111">Elements and attributes</span></span>

<span data-ttu-id="fcb41-112">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fcb41-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fcb41-113">親要素</span><span class="sxs-lookup"><span data-stu-id="fcb41-113">Parent elements</span></span>

<span data-ttu-id="fcb41-114">なし。</span><span class="sxs-lookup"><span data-stu-id="fcb41-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fcb41-115">子要素</span><span class="sxs-lookup"><span data-stu-id="fcb41-115">Child elements</span></span>

|<span data-ttu-id="fcb41-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="fcb41-116">**Element**</span></span>|<span data-ttu-id="fcb41-117">**型**</span><span class="sxs-lookup"><span data-stu-id="fcb41-117">**Type**</span></span>|<span data-ttu-id="fcb41-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="fcb41-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fcb41-119">天気</span><span class="sxs-lookup"><span data-stu-id="fcb41-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="fcb41-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="fcb41-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="fcb41-121">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="fcb41-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fcb41-122">属性</span><span class="sxs-lookup"><span data-stu-id="fcb41-122">Attributes</span></span>

<span data-ttu-id="fcb41-123">なし。</span><span class="sxs-lookup"><span data-stu-id="fcb41-123">None.</span></span>
  

