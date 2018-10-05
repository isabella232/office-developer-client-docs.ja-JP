---
title: PrimaryKey_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 679c6335d89855febd82bdeb6e9ac88f4089e1c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391368"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="c10b5-102">PrimaryKey_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c10b5-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c10b5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c10b5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c10b5-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c10b5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c10b5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c10b5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c10b5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c10b5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c10b5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c10b5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c10b5-108">なし</span><span class="sxs-lookup"><span data-stu-id="c10b5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c10b5-109">定義</span><span class="sxs-lookup"><span data-stu-id="c10b5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c10b5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c10b5-110">Elements and attributes</span></span>

<span data-ttu-id="c10b5-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c10b5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c10b5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c10b5-112">Child elements</span></span>

|<span data-ttu-id="c10b5-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="c10b5-113">**Element**</span></span>|<span data-ttu-id="c10b5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c10b5-114">**Type**</span></span>|<span data-ttu-id="c10b5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c10b5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c10b5-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="c10b5-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c10b5-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="c10b5-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c10b5-118">属性</span><span class="sxs-lookup"><span data-stu-id="c10b5-118">Attributes</span></span>

|<span data-ttu-id="c10b5-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="c10b5-119">**Attribute**</span></span>|<span data-ttu-id="c10b5-120">**型**</span><span class="sxs-lookup"><span data-stu-id="c10b5-120">**Type**</span></span>|<span data-ttu-id="c10b5-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="c10b5-121">**Required**</span></span>|<span data-ttu-id="c10b5-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="c10b5-122">**Description**</span></span>|<span data-ttu-id="c10b5-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c10b5-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c10b5-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="c10b5-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="c10b5-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c10b5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c10b5-126">必須</span><span class="sxs-lookup"><span data-stu-id="c10b5-126">required</span></span>  <br/> ||<span data-ttu-id="c10b5-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c10b5-127">Values of the xsd:string type.</span></span>  <br/> |
   

