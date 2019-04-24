---
title: DataColumns_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344598"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="07cdd-102">DataColumns_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="07cdd-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="07cdd-103">型情報</span><span class="sxs-lookup"><span data-stu-id="07cdd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07cdd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="07cdd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="07cdd-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="07cdd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="07cdd-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="07cdd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="07cdd-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="07cdd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="07cdd-108">なし</span><span class="sxs-lookup"><span data-stu-id="07cdd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="07cdd-109">定義</span><span class="sxs-lookup"><span data-stu-id="07cdd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="07cdd-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="07cdd-110">Elements and attributes</span></span>

<span data-ttu-id="07cdd-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="07cdd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="07cdd-112">子要素</span><span class="sxs-lookup"><span data-stu-id="07cdd-112">Child elements</span></span>

|<span data-ttu-id="07cdd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="07cdd-113">**Element**</span></span>|<span data-ttu-id="07cdd-114">**型**</span><span class="sxs-lookup"><span data-stu-id="07cdd-114">**Type**</span></span>|<span data-ttu-id="07cdd-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="07cdd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="07cdd-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="07cdd-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="07cdd-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="07cdd-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="07cdd-118">属性</span><span class="sxs-lookup"><span data-stu-id="07cdd-118">Attributes</span></span>

|<span data-ttu-id="07cdd-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="07cdd-119">**Attribute**</span></span>|<span data-ttu-id="07cdd-120">**型**</span><span class="sxs-lookup"><span data-stu-id="07cdd-120">**Type**</span></span>|<span data-ttu-id="07cdd-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="07cdd-121">**Required**</span></span>|<span data-ttu-id="07cdd-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="07cdd-122">**Description**</span></span>|<span data-ttu-id="07cdd-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="07cdd-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="07cdd-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="07cdd-124">SortAsc</span></span>  <br/> |<span data-ttu-id="07cdd-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="07cdd-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="07cdd-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="07cdd-126">optional</span></span>  <br/> ||<span data-ttu-id="07cdd-127">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="07cdd-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="07cdd-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="07cdd-128">SortColumn</span></span>  <br/> |<span data-ttu-id="07cdd-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="07cdd-129">xsd:string</span></span>  <br/> |<span data-ttu-id="07cdd-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="07cdd-130">optional</span></span>  <br/> ||<span data-ttu-id="07cdd-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="07cdd-131">Values of the xsd:string type.</span></span>  <br/> |
   

