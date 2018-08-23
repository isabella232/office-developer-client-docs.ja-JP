---
title: weatherType complexType (Outlook の天気予報の場所のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: 場所の気象条件のパラメーターを定義します。
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804558"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="622a6-103">weatherType complexType (Outlook の天気予報の場所のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="622a6-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="622a6-104">場所の気象条件のパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="622a6-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="622a6-105">型情報</span><span class="sxs-lookup"><span data-stu-id="622a6-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="622a6-106">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="622a6-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="622a6-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="622a6-107">**Schema file**</span></span> <br/> |<span data-ttu-id="622a6-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="622a6-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="622a6-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="622a6-109">**Extension base**</span></span> <br/> |<span data-ttu-id="622a6-110">なし</span><span class="sxs-lookup"><span data-stu-id="622a6-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="622a6-111">定義</span><span class="sxs-lookup"><span data-stu-id="622a6-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="622a6-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="622a6-112">Elements and attributes</span></span>

<span data-ttu-id="622a6-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="622a6-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="622a6-114">子要素</span><span class="sxs-lookup"><span data-stu-id="622a6-114">Child elements</span></span>

<span data-ttu-id="622a6-115">なし。</span><span class="sxs-lookup"><span data-stu-id="622a6-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="622a6-116">属性</span><span class="sxs-lookup"><span data-stu-id="622a6-116">Attributes</span></span>

|<span data-ttu-id="622a6-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="622a6-117">**Attribute**</span></span>|<span data-ttu-id="622a6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="622a6-118">**Type**</span></span>|<span data-ttu-id="622a6-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="622a6-119">**Required**</span></span>|<span data-ttu-id="622a6-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="622a6-120">**Description**</span></span>|<span data-ttu-id="622a6-121">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="622a6-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="622a6-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="622a6-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="622a6-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="622a6-123">xs:string</span></span>  <br/> |<span data-ttu-id="622a6-124">必須</span><span class="sxs-lookup"><span data-stu-id="622a6-124">required</span></span>  <br/> |<span data-ttu-id="622a6-125">同じ名前の複数の場所を識別するために場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="622a6-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="622a6-126">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="622a6-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="622a6-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="622a6-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="622a6-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="622a6-128">xs:string</span></span>  <br/> |<span data-ttu-id="622a6-129">必須</span><span class="sxs-lookup"><span data-stu-id="622a6-129">required</span></span>  <br/> |<span data-ttu-id="622a6-130">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="622a6-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="622a6-131">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="622a6-131">A value of the type xs:string</span></span>  <br/> |
   

