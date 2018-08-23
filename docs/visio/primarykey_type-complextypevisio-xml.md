---
title: PrimaryKey_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2d13ac2b6d55fdda752f16af28a0843d5a388f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806108"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="4c520-102">PrimaryKey_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4c520-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4c520-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4c520-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c520-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4c520-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4c520-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4c520-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4c520-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4c520-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4c520-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="4c520-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4c520-108">なし</span><span class="sxs-lookup"><span data-stu-id="4c520-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c520-109">定義</span><span class="sxs-lookup"><span data-stu-id="4c520-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4c520-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4c520-110">Elements and attributes</span></span>

<span data-ttu-id="4c520-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c520-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4c520-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4c520-112">Child elements</span></span>

|<span data-ttu-id="4c520-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="4c520-113">**Element**</span></span>|<span data-ttu-id="4c520-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4c520-114">**Type**</span></span>|<span data-ttu-id="4c520-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4c520-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c520-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="4c520-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c520-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="4c520-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4c520-118">属性</span><span class="sxs-lookup"><span data-stu-id="4c520-118">Attributes</span></span>

|<span data-ttu-id="4c520-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="4c520-119">**Attribute**</span></span>|<span data-ttu-id="4c520-120">**型**</span><span class="sxs-lookup"><span data-stu-id="4c520-120">**Type**</span></span>|<span data-ttu-id="4c520-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="4c520-121">**Required**</span></span>|<span data-ttu-id="4c520-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="4c520-122">**Description**</span></span>|<span data-ttu-id="4c520-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4c520-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4c520-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="4c520-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="4c520-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4c520-125">xsd:string</span></span>  <br/> |<span data-ttu-id="4c520-126">必須</span><span class="sxs-lookup"><span data-stu-id="4c520-126">required</span></span>  <br/> ||<span data-ttu-id="4c520-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c520-127">Values of the xsd:string type.</span></span>  <br/> |
   

