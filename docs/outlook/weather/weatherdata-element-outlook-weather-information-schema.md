---
title: weatherdata 要素 (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: 天気予報の要素を定義します。
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355077"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="6e365-103">weatherdata 要素 (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="6e365-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="6e365-104">天気予報の要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="6e365-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e365-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6e365-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e365-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6e365-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="6e365-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6e365-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="6e365-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6e365-108">**Schema file**</span></span> <br/> |<span data-ttu-id="6e365-109">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="6e365-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e365-110">定義</span><span class="sxs-lookup"><span data-stu-id="6e365-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6e365-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6e365-111">Elements and attributes</span></span>

<span data-ttu-id="6e365-112">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e365-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6e365-113">親要素</span><span class="sxs-lookup"><span data-stu-id="6e365-113">Parent elements</span></span>

<span data-ttu-id="6e365-114">なし。</span><span class="sxs-lookup"><span data-stu-id="6e365-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e365-115">子要素</span><span class="sxs-lookup"><span data-stu-id="6e365-115">Child elements</span></span>

|<span data-ttu-id="6e365-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e365-116">**Element**</span></span>|<span data-ttu-id="6e365-117">**型**</span><span class="sxs-lookup"><span data-stu-id="6e365-117">**Type**</span></span>|<span data-ttu-id="6e365-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6e365-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e365-119">天気予報</span><span class="sxs-lookup"><span data-stu-id="6e365-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="6e365-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="6e365-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="6e365-121">場所の天気予報の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e365-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6e365-122">属性</span><span class="sxs-lookup"><span data-stu-id="6e365-122">Attributes</span></span>

<span data-ttu-id="6e365-123">なし。</span><span class="sxs-lookup"><span data-stu-id="6e365-123">None.</span></span>
  

