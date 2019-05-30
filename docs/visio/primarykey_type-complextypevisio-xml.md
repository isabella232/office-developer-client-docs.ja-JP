---
title: PrimaryKey_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2e8b1a8238133bf579dadf80363a70be949f48d2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538796"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="c4015-102">PrimaryKey_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c4015-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c4015-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c4015-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4015-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4015-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4015-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c4015-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4015-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="c4015-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4015-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c4015-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4015-108">None</span><span class="sxs-lookup"><span data-stu-id="c4015-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4015-109">定義</span><span class="sxs-lookup"><span data-stu-id="c4015-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c4015-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c4015-110">Elements and attributes</span></span>

<span data-ttu-id="c4015-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4015-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4015-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c4015-112">Child elements</span></span>

|<span data-ttu-id="c4015-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4015-113">**Element**</span></span>|<span data-ttu-id="c4015-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c4015-114">**Type**</span></span>|<span data-ttu-id="c4015-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c4015-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4015-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="c4015-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c4015-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="c4015-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c4015-118">属性</span><span class="sxs-lookup"><span data-stu-id="c4015-118">Attributes</span></span>

|<span data-ttu-id="c4015-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="c4015-119">**Attribute**</span></span>|<span data-ttu-id="c4015-120">**型**</span><span class="sxs-lookup"><span data-stu-id="c4015-120">**Type**</span></span>|<span data-ttu-id="c4015-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="c4015-121">**Required**</span></span>|<span data-ttu-id="c4015-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="c4015-122">**Description**</span></span>|<span data-ttu-id="c4015-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c4015-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4015-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="c4015-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="c4015-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c4015-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c4015-126">必須</span><span class="sxs-lookup"><span data-stu-id="c4015-126">required</span></span>  <br/> ||<span data-ttu-id="c4015-127">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c4015-127">Values of the xsd:string type.</span></span>  <br/> |
   

