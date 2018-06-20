---
title: RefreshableData 要素 (PublishSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: レコード セットは、Microsoft SharePoint Server 2013 で Visio Services を使用してデータを更新するかどうかを指定します。
ms.openlocfilehash: 47da60fb95b49084b70cfc630430879f04463553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806159"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="62172-103">RefreshableData 要素 (PublishSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="62172-103">RefreshableData element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="62172-104">レコード セットは、Microsoft SharePoint Server 2013 で Visio Services を使用してデータを更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="62172-104">Specifies whether a recordset is refreshable using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62172-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="62172-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62172-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="62172-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62172-107">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="62172-107">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62172-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="62172-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62172-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="62172-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62172-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="62172-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62172-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="62172-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62172-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="62172-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62172-113">定義</span><span class="sxs-lookup"><span data-stu-id="62172-113">Definition</span></span>

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a><span data-ttu-id="62172-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="62172-114">Elements and attributes</span></span>

<span data-ttu-id="62172-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="62172-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62172-116">親要素</span><span class="sxs-lookup"><span data-stu-id="62172-116">Parent elements</span></span>

|<span data-ttu-id="62172-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="62172-117">**Element**</span></span>|<span data-ttu-id="62172-118">**型**</span><span class="sxs-lookup"><span data-stu-id="62172-118">**Type**</span></span>|<span data-ttu-id="62172-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="62172-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62172-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="62172-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62172-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="62172-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62172-122">Visio Services を使用して、ダイアグラムを開いたときに使用する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="62172-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62172-123">子要素</span><span class="sxs-lookup"><span data-stu-id="62172-123">Child elements</span></span>

<span data-ttu-id="62172-124">なし。</span><span class="sxs-lookup"><span data-stu-id="62172-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62172-125">属性</span><span class="sxs-lookup"><span data-stu-id="62172-125">Attributes</span></span>

|<span data-ttu-id="62172-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="62172-126">**Attribute**</span></span>|<span data-ttu-id="62172-127">**型**</span><span class="sxs-lookup"><span data-stu-id="62172-127">**Type**</span></span>|<span data-ttu-id="62172-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="62172-128">**Required**</span></span>|<span data-ttu-id="62172-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="62172-129">**Description**</span></span>|<span data-ttu-id="62172-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="62172-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62172-131">ID</span><span class="sxs-lookup"><span data-stu-id="62172-131">ID</span></span>  <br/> |<span data-ttu-id="62172-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="62172-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="62172-133">必須</span><span class="sxs-lookup"><span data-stu-id="62172-133">required</span></span>  <br/> |<span data-ttu-id="62172-134">レコード セットの識別子です。</span><span class="sxs-lookup"><span data-stu-id="62172-134">The identifier of a recordset.</span></span>  <br/> |<span data-ttu-id="62172-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="62172-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

