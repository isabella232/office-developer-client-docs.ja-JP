---
title: DataConnections 要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: ドキュメントの DataConnection 要素が含まれています。
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395029"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="cafb5-103">DataConnections 要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="cafb5-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="cafb5-104">ドキュメントの**DataConnection**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cafb5-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cafb5-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="cafb5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cafb5-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="cafb5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cafb5-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="cafb5-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cafb5-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cafb5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cafb5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cafb5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cafb5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cafb5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cafb5-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="cafb5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cafb5-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="cafb5-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cafb5-113">定義</span><span class="sxs-lookup"><span data-stu-id="cafb5-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cafb5-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cafb5-114">Elements and attributes</span></span>

<span data-ttu-id="cafb5-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cafb5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cafb5-116">親要素</span><span class="sxs-lookup"><span data-stu-id="cafb5-116">Parent elements</span></span>

<span data-ttu-id="cafb5-117">なし。</span><span class="sxs-lookup"><span data-stu-id="cafb5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cafb5-118">子要素</span><span class="sxs-lookup"><span data-stu-id="cafb5-118">Child elements</span></span>

|<span data-ttu-id="cafb5-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="cafb5-119">**Element**</span></span>|<span data-ttu-id="cafb5-120">**型**</span><span class="sxs-lookup"><span data-stu-id="cafb5-120">**Type**</span></span>|<span data-ttu-id="cafb5-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="cafb5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cafb5-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="cafb5-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cafb5-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="cafb5-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cafb5-124">1 つまたは複数の**データ レコード セット**の要素と XML 以外のデータ ソース間の通信を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="cafb5-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cafb5-125">属性</span><span class="sxs-lookup"><span data-stu-id="cafb5-125">Attributes</span></span>

|<span data-ttu-id="cafb5-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="cafb5-126">**Attribute**</span></span>|<span data-ttu-id="cafb5-127">**型**</span><span class="sxs-lookup"><span data-stu-id="cafb5-127">**Type**</span></span>|<span data-ttu-id="cafb5-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="cafb5-128">**Required**</span></span>|<span data-ttu-id="cafb5-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="cafb5-129">**Description**</span></span>|<span data-ttu-id="cafb5-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="cafb5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cafb5-131">NextID</span><span class="sxs-lookup"><span data-stu-id="cafb5-131">NextID</span></span>  <br/> |<span data-ttu-id="cafb5-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cafb5-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cafb5-133">必須</span><span class="sxs-lookup"><span data-stu-id="cafb5-133">required</span></span>  <br/> |<span data-ttu-id="cafb5-134">新しい接続のため次の使用可能な ID です。</span><span class="sxs-lookup"><span data-stu-id="cafb5-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="cafb5-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cafb5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

