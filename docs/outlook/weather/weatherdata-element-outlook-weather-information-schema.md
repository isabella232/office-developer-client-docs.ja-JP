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
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388442"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="e0f3e-103">weatherdata 要素 (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="e0f3e-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="e0f3e-104">気象要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="e0f3e-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0f3e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e0f3e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0f3e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="e0f3e-107">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="e0f3e-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-108">**Schema file**</span></span> <br/> |<span data-ttu-id="e0f3e-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="e0f3e-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0f3e-110">定義</span><span class="sxs-lookup"><span data-stu-id="e0f3e-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e0f3e-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e0f3e-111">Elements and attributes</span></span>

<span data-ttu-id="e0f3e-112">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0f3e-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e0f3e-113">親要素</span><span class="sxs-lookup"><span data-stu-id="e0f3e-113">Parent elements</span></span>

<span data-ttu-id="e0f3e-114">なし。</span><span class="sxs-lookup"><span data-stu-id="e0f3e-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0f3e-115">子要素</span><span class="sxs-lookup"><span data-stu-id="e0f3e-115">Child elements</span></span>

|<span data-ttu-id="e0f3e-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-116">**Element**</span></span>|<span data-ttu-id="e0f3e-117">**型**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-117">**Type**</span></span>|<span data-ttu-id="e0f3e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0f3e-119">天気</span><span class="sxs-lookup"><span data-stu-id="e0f3e-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="e0f3e-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="e0f3e-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="e0f3e-121">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0f3e-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e0f3e-122">属性</span><span class="sxs-lookup"><span data-stu-id="e0f3e-122">Attributes</span></span>

<span data-ttu-id="e0f3e-123">なし。</span><span class="sxs-lookup"><span data-stu-id="e0f3e-123">None.</span></span>
  

