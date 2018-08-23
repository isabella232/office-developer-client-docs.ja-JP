---
title: weatherdata 要素 (Outlook の天気予報の場所のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: 気象要素を定義します。
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804575"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="71b36-103">weatherdata 要素 (Outlook の天気予報の場所のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="71b36-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="71b36-104">気象要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="71b36-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71b36-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="71b36-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71b36-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="71b36-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="71b36-107">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="71b36-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="71b36-108">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="71b36-108">**Schema file**</span></span> <br/> |<span data-ttu-id="71b36-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="71b36-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71b36-110">定義</span><span class="sxs-lookup"><span data-stu-id="71b36-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="71b36-111">要素と属性</span><span class="sxs-lookup"><span data-stu-id="71b36-111">Elements and attributes</span></span>

<span data-ttu-id="71b36-112">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="71b36-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="71b36-113">親要素</span><span class="sxs-lookup"><span data-stu-id="71b36-113">Parent elements</span></span>

<span data-ttu-id="71b36-114">なし。</span><span class="sxs-lookup"><span data-stu-id="71b36-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="71b36-115">子要素</span><span class="sxs-lookup"><span data-stu-id="71b36-115">Child elements</span></span>

|<span data-ttu-id="71b36-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="71b36-116">**Element**</span></span>|<span data-ttu-id="71b36-117">**型**</span><span class="sxs-lookup"><span data-stu-id="71b36-117">**Type**</span></span>|<span data-ttu-id="71b36-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="71b36-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71b36-119">天気</span><span class="sxs-lookup"><span data-stu-id="71b36-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="71b36-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="71b36-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="71b36-121">天気をレポートする場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="71b36-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="71b36-122">属性</span><span class="sxs-lookup"><span data-stu-id="71b36-122">Attributes</span></span>

<span data-ttu-id="71b36-123">なし。</span><span class="sxs-lookup"><span data-stu-id="71b36-123">None.</span></span>
  

