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
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538985"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="2aa2b-103">weatherdata 要素 (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="2aa2b-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="2aa2b-104">天気予報の要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="2aa2b-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2aa2b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="2aa2b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2aa2b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="2aa2b-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="2aa2b-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-108">**Schema file**</span></span> <br/> |<span data-ttu-id="2aa2b-109">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="2aa2b-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2aa2b-110">定義</span><span class="sxs-lookup"><span data-stu-id="2aa2b-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2aa2b-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2aa2b-111">Elements and attributes</span></span>

<span data-ttu-id="2aa2b-112">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2aa2b-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2aa2b-113">親要素</span><span class="sxs-lookup"><span data-stu-id="2aa2b-113">Parent elements</span></span>

<span data-ttu-id="2aa2b-114">なし。</span><span class="sxs-lookup"><span data-stu-id="2aa2b-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2aa2b-115">子要素</span><span class="sxs-lookup"><span data-stu-id="2aa2b-115">Child elements</span></span>

|<span data-ttu-id="2aa2b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-116">**Element**</span></span>|<span data-ttu-id="2aa2b-117">**型**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-117">**Type**</span></span>|<span data-ttu-id="2aa2b-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2aa2b-119">天気予報</span><span class="sxs-lookup"><span data-stu-id="2aa2b-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="2aa2b-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="2aa2b-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="2aa2b-121">場所の天気予報の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="2aa2b-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2aa2b-122">属性</span><span class="sxs-lookup"><span data-stu-id="2aa2b-122">Attributes</span></span>

<span data-ttu-id="2aa2b-123">なし。</span><span class="sxs-lookup"><span data-stu-id="2aa2b-123">None.</span></span>
  

