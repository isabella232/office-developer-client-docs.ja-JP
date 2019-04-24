---
title: DataConnections_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 2bbea48e1d5340c5a68bbafbef9a900a98357385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360376"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="0a9ab-102">DataConnections_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0a9ab-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0a9ab-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0a9ab-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a9ab-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a9ab-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a9ab-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="0a9ab-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a9ab-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a9ab-108">なし</span><span class="sxs-lookup"><span data-stu-id="0a9ab-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a9ab-109">定義</span><span class="sxs-lookup"><span data-stu-id="0a9ab-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0a9ab-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0a9ab-110">Elements and attributes</span></span>

<span data-ttu-id="0a9ab-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a9ab-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0a9ab-112">Child elements</span></span>

|<span data-ttu-id="0a9ab-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-113">**Element**</span></span>|<span data-ttu-id="0a9ab-114">**型**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-114">**Type**</span></span>|<span data-ttu-id="0a9ab-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a9ab-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="0a9ab-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0a9ab-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="0a9ab-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0a9ab-118">属性</span><span class="sxs-lookup"><span data-stu-id="0a9ab-118">Attributes</span></span>

|<span data-ttu-id="0a9ab-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-119">**Attribute**</span></span>|<span data-ttu-id="0a9ab-120">**型**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-120">**Type**</span></span>|<span data-ttu-id="0a9ab-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-121">**Required**</span></span>|<span data-ttu-id="0a9ab-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-122">**Description**</span></span>|<span data-ttu-id="0a9ab-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0a9ab-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a9ab-124">NextID</span><span class="sxs-lookup"><span data-stu-id="0a9ab-124">NextID</span></span>  <br/> |<span data-ttu-id="0a9ab-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="0a9ab-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a9ab-126">必須</span><span class="sxs-lookup"><span data-stu-id="0a9ab-126">required</span></span>  <br/> ||<span data-ttu-id="0a9ab-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

