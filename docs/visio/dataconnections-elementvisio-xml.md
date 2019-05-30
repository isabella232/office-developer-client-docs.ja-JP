---
title: DataConnections 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: 文書の DataConnection 要素を格納します。
ms.openlocfilehash: 5d45d1dcd76524c2144336235e8277cd51f8a138
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539183"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="95843-103">DataConnections 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="95843-103">DataConnections element (Visio XML)</span></span>

<span data-ttu-id="95843-104">文書の**DataConnection**要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="95843-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="95843-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="95843-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95843-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="95843-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95843-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="95843-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95843-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95843-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95843-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="95843-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95843-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="95843-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95843-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="95843-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95843-112">接続 xml</span><span class="sxs-lookup"><span data-stu-id="95843-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95843-113">定義</span><span class="sxs-lookup"><span data-stu-id="95843-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95843-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="95843-114">Elements and attributes</span></span>

<span data-ttu-id="95843-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="95843-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95843-116">親要素</span><span class="sxs-lookup"><span data-stu-id="95843-116">Parent elements</span></span>

<span data-ttu-id="95843-117">なし。</span><span class="sxs-lookup"><span data-stu-id="95843-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95843-118">子要素</span><span class="sxs-lookup"><span data-stu-id="95843-118">Child elements</span></span>

|<span data-ttu-id="95843-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="95843-119">**Element**</span></span>|<span data-ttu-id="95843-120">**型**</span><span class="sxs-lookup"><span data-stu-id="95843-120">**Type**</span></span>|<span data-ttu-id="95843-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="95843-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95843-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="95843-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95843-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="95843-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95843-124">1つまたは複数の**DataRecordset**要素と非 XML データソース間の情報を抽出します。</span><span class="sxs-lookup"><span data-stu-id="95843-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95843-125">属性</span><span class="sxs-lookup"><span data-stu-id="95843-125">Attributes</span></span>

|<span data-ttu-id="95843-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="95843-126">**Attribute**</span></span>|<span data-ttu-id="95843-127">**型**</span><span class="sxs-lookup"><span data-stu-id="95843-127">**Type**</span></span>|<span data-ttu-id="95843-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="95843-128">**Required**</span></span>|<span data-ttu-id="95843-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="95843-129">**Description**</span></span>|<span data-ttu-id="95843-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="95843-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95843-131">NextID</span><span class="sxs-lookup"><span data-stu-id="95843-131">NextID</span></span>  <br/> |<span data-ttu-id="95843-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="95843-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95843-133">必須</span><span class="sxs-lookup"><span data-stu-id="95843-133">required</span></span>  <br/> |<span data-ttu-id="95843-134">新しい接続に対して使用可能な次の ID。</span><span class="sxs-lookup"><span data-stu-id="95843-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="95843-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="95843-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

