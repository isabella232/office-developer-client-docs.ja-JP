---
title: RefreshableData 要素 (PublishSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: Microsoft SharePoint Server 2013 の Visio Services を使用して recordset を更新可能にするかどうかを指定します。
ms.openlocfilehash: 21a0a5c198998c4b230be88c6bd9f96b25265990
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542878"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="54fa2-103">RefreshableData 要素 (PublishSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="54fa2-103">RefreshableData element (PublishSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="54fa2-104">Microsoft SharePoint Server 2013 の Visio Services を使用して recordset を更新可能にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fa2-104">Specifies whether a recordset is refreshable using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54fa2-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="54fa2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54fa2-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="54fa2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="54fa2-107">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="54fa2-107">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="54fa2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="54fa2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="54fa2-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="54fa2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="54fa2-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="54fa2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="54fa2-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="54fa2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="54fa2-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="54fa2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54fa2-113">定義</span><span class="sxs-lookup"><span data-stu-id="54fa2-113">Definition</span></span>

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a><span data-ttu-id="54fa2-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="54fa2-114">Elements and attributes</span></span>

<span data-ttu-id="54fa2-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fa2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="54fa2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="54fa2-116">Parent elements</span></span>

|<span data-ttu-id="54fa2-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="54fa2-117">**Element**</span></span>|<span data-ttu-id="54fa2-118">**型**</span><span class="sxs-lookup"><span data-stu-id="54fa2-118">**Type**</span></span>|<span data-ttu-id="54fa2-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="54fa2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54fa2-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="54fa2-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54fa2-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="54fa2-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54fa2-122">Visio Services を使用して図面を開くときに使用する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="54fa2-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54fa2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="54fa2-123">Child elements</span></span>

<span data-ttu-id="54fa2-124">なし。</span><span class="sxs-lookup"><span data-stu-id="54fa2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54fa2-125">属性</span><span class="sxs-lookup"><span data-stu-id="54fa2-125">Attributes</span></span>

|<span data-ttu-id="54fa2-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="54fa2-126">**Attribute**</span></span>|<span data-ttu-id="54fa2-127">**型**</span><span class="sxs-lookup"><span data-stu-id="54fa2-127">**Type**</span></span>|<span data-ttu-id="54fa2-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="54fa2-128">**Required**</span></span>|<span data-ttu-id="54fa2-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="54fa2-129">**Description**</span></span>|<span data-ttu-id="54fa2-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="54fa2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="54fa2-131">ID</span><span class="sxs-lookup"><span data-stu-id="54fa2-131">ID</span></span>  <br/> |<span data-ttu-id="54fa2-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="54fa2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54fa2-133">必須</span><span class="sxs-lookup"><span data-stu-id="54fa2-133">required</span></span>  <br/> |<span data-ttu-id="54fa2-134">Recordset の識別子。</span><span class="sxs-lookup"><span data-stu-id="54fa2-134">The identifier of a recordset.</span></span>  <br/> |<span data-ttu-id="54fa2-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="54fa2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

