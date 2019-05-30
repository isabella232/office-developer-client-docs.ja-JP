---
title: DataConnections_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 712632a74b0ffad6d0c9ca8745d67018518d87de
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542458"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="603f3-102">DataConnections_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="603f3-102">DataConnections_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="603f3-103">型情報</span><span class="sxs-lookup"><span data-stu-id="603f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="603f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="603f3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="603f3-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="603f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="603f3-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="603f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="603f3-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="603f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="603f3-108">None</span><span class="sxs-lookup"><span data-stu-id="603f3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="603f3-109">定義</span><span class="sxs-lookup"><span data-stu-id="603f3-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="603f3-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="603f3-110">Elements and attributes</span></span>

<span data-ttu-id="603f3-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="603f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="603f3-112">子要素</span><span class="sxs-lookup"><span data-stu-id="603f3-112">Child elements</span></span>

|<span data-ttu-id="603f3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="603f3-113">**Element**</span></span>|<span data-ttu-id="603f3-114">**型**</span><span class="sxs-lookup"><span data-stu-id="603f3-114">**Type**</span></span>|<span data-ttu-id="603f3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="603f3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="603f3-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="603f3-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="603f3-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="603f3-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="603f3-118">属性</span><span class="sxs-lookup"><span data-stu-id="603f3-118">Attributes</span></span>

|<span data-ttu-id="603f3-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="603f3-119">**Attribute**</span></span>|<span data-ttu-id="603f3-120">**型**</span><span class="sxs-lookup"><span data-stu-id="603f3-120">**Type**</span></span>|<span data-ttu-id="603f3-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="603f3-121">**Required**</span></span>|<span data-ttu-id="603f3-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="603f3-122">**Description**</span></span>|<span data-ttu-id="603f3-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="603f3-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="603f3-124">NextID</span><span class="sxs-lookup"><span data-stu-id="603f3-124">NextID</span></span>  <br/> |<span data-ttu-id="603f3-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="603f3-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="603f3-126">必須</span><span class="sxs-lookup"><span data-stu-id="603f3-126">required</span></span>  <br/> ||<span data-ttu-id="603f3-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="603f3-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

