---
title: RefreshableData 要素 (PublishSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: レコード セットは、Microsoft SharePoint Server 2013 で Visio Services を使用してデータを更新するかどうかを指定します。
ms.openlocfilehash: b402e2c9d65bf868c0ac33c782b87857ab6aed75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384873"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="561ee-103">RefreshableData 要素 (PublishSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="561ee-103">RefreshableData element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="561ee-104">レコード セットは、Microsoft SharePoint Server 2013 で Visio Services を使用してデータを更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="561ee-104">Specifies whether a recordset is refreshable using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="561ee-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="561ee-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="561ee-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="561ee-106">**Element type**</span></span> <br/> |[<span data-ttu-id="561ee-107">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="561ee-107">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="561ee-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="561ee-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="561ee-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="561ee-109">**Schema file**</span></span> <br/> |<span data-ttu-id="561ee-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="561ee-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="561ee-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="561ee-111">**Document parts**</span></span> <br/> |<span data-ttu-id="561ee-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="561ee-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="561ee-113">定義</span><span class="sxs-lookup"><span data-stu-id="561ee-113">Definition</span></span>

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a><span data-ttu-id="561ee-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="561ee-114">Elements and attributes</span></span>

<span data-ttu-id="561ee-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="561ee-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="561ee-116">親要素</span><span class="sxs-lookup"><span data-stu-id="561ee-116">Parent elements</span></span>

|<span data-ttu-id="561ee-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="561ee-117">**Element**</span></span>|<span data-ttu-id="561ee-118">**型**</span><span class="sxs-lookup"><span data-stu-id="561ee-118">**Type**</span></span>|<span data-ttu-id="561ee-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="561ee-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="561ee-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="561ee-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="561ee-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="561ee-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="561ee-122">Visio Services を使用して、ダイアグラムを開いたときに使用する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="561ee-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="561ee-123">子要素</span><span class="sxs-lookup"><span data-stu-id="561ee-123">Child elements</span></span>

<span data-ttu-id="561ee-124">なし。</span><span class="sxs-lookup"><span data-stu-id="561ee-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="561ee-125">属性</span><span class="sxs-lookup"><span data-stu-id="561ee-125">Attributes</span></span>

|<span data-ttu-id="561ee-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="561ee-126">**Attribute**</span></span>|<span data-ttu-id="561ee-127">**型**</span><span class="sxs-lookup"><span data-stu-id="561ee-127">**Type**</span></span>|<span data-ttu-id="561ee-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="561ee-128">**Required**</span></span>|<span data-ttu-id="561ee-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="561ee-129">**Description**</span></span>|<span data-ttu-id="561ee-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="561ee-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="561ee-131">ID</span><span class="sxs-lookup"><span data-stu-id="561ee-131">ID</span></span>  <br/> |<span data-ttu-id="561ee-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="561ee-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="561ee-133">必須</span><span class="sxs-lookup"><span data-stu-id="561ee-133">required</span></span>  <br/> |<span data-ttu-id="561ee-134">レコード セットの識別子です。</span><span class="sxs-lookup"><span data-stu-id="561ee-134">The identifier of a recordset.</span></span>  <br/> |<span data-ttu-id="561ee-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="561ee-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

