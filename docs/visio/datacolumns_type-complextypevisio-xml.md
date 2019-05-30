---
title: DataColumns_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: ffe0fbfeaf0b0b67386a6cadd1beb78058819d39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541149"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="3e474-102">DataColumns_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3e474-102">DataColumns_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3e474-103">型情報</span><span class="sxs-lookup"><span data-stu-id="3e474-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e474-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3e474-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3e474-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3e474-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3e474-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="3e474-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3e474-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="3e474-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3e474-108">None</span><span class="sxs-lookup"><span data-stu-id="3e474-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e474-109">定義</span><span class="sxs-lookup"><span data-stu-id="3e474-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3e474-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3e474-110">Elements and attributes</span></span>

<span data-ttu-id="3e474-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e474-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3e474-112">子要素</span><span class="sxs-lookup"><span data-stu-id="3e474-112">Child elements</span></span>

|<span data-ttu-id="3e474-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e474-113">**Element**</span></span>|<span data-ttu-id="3e474-114">**型**</span><span class="sxs-lookup"><span data-stu-id="3e474-114">**Type**</span></span>|<span data-ttu-id="3e474-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e474-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e474-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="3e474-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e474-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="3e474-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3e474-118">属性</span><span class="sxs-lookup"><span data-stu-id="3e474-118">Attributes</span></span>

|<span data-ttu-id="3e474-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="3e474-119">**Attribute**</span></span>|<span data-ttu-id="3e474-120">**型**</span><span class="sxs-lookup"><span data-stu-id="3e474-120">**Type**</span></span>|<span data-ttu-id="3e474-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="3e474-121">**Required**</span></span>|<span data-ttu-id="3e474-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e474-122">**Description**</span></span>|<span data-ttu-id="3e474-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3e474-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3e474-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="3e474-124">SortAsc</span></span>  <br/> |<span data-ttu-id="3e474-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="3e474-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3e474-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="3e474-126">optional</span></span>  <br/> ||<span data-ttu-id="3e474-127">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="3e474-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3e474-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="3e474-128">SortColumn</span></span>  <br/> |<span data-ttu-id="3e474-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3e474-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3e474-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="3e474-130">optional</span></span>  <br/> ||<span data-ttu-id="3e474-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3e474-131">Values of the xsd:string type.</span></span>  <br/> |
   

