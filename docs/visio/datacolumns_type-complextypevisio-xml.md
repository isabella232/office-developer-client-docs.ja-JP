---
title: DataColumns_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382380"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="9d5e3-102">DataColumns_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="9d5e3-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9d5e3-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9d5e3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d5e3-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9d5e3-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9d5e3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9d5e3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9d5e3-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9d5e3-108">なし</span><span class="sxs-lookup"><span data-stu-id="9d5e3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d5e3-109">定義</span><span class="sxs-lookup"><span data-stu-id="9d5e3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9d5e3-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9d5e3-110">Elements and attributes</span></span>

<span data-ttu-id="9d5e3-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d5e3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9d5e3-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9d5e3-112">Child elements</span></span>

|<span data-ttu-id="9d5e3-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-113">**Element**</span></span>|<span data-ttu-id="9d5e3-114">**型**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-114">**Type**</span></span>|<span data-ttu-id="9d5e3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d5e3-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="9d5e3-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d5e3-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="9d5e3-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9d5e3-118">属性</span><span class="sxs-lookup"><span data-stu-id="9d5e3-118">Attributes</span></span>

|<span data-ttu-id="9d5e3-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-119">**Attribute**</span></span>|<span data-ttu-id="9d5e3-120">**型**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-120">**Type**</span></span>|<span data-ttu-id="9d5e3-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-121">**Required**</span></span>|<span data-ttu-id="9d5e3-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-122">**Description**</span></span>|<span data-ttu-id="9d5e3-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9d5e3-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d5e3-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="9d5e3-124">SortAsc</span></span>  <br/> |<span data-ttu-id="9d5e3-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9d5e3-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9d5e3-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="9d5e3-126">optional</span></span>  <br/> ||<span data-ttu-id="9d5e3-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d5e3-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9d5e3-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="9d5e3-128">SortColumn</span></span>  <br/> |<span data-ttu-id="9d5e3-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d5e3-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9d5e3-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="9d5e3-130">optional</span></span>  <br/> ||<span data-ttu-id="9d5e3-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d5e3-131">Values of the xsd:string type.</span></span>  <br/> |
   

