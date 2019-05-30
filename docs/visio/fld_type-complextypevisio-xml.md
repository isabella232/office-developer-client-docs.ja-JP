---
title: fld_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 5651a0b0a2d09e3fbbdb0d1dbf66f1be3d374c12
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539601"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="9c326-102">fld_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9c326-102">fld_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9c326-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9c326-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c326-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c326-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c326-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9c326-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c326-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="9c326-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c326-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="9c326-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c326-108">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9c326-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c326-109">定義</span><span class="sxs-lookup"><span data-stu-id="9c326-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c326-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9c326-110">Elements and attributes</span></span>

<span data-ttu-id="9c326-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c326-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c326-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9c326-112">Child elements</span></span>

<span data-ttu-id="9c326-113">なし。</span><span class="sxs-lookup"><span data-stu-id="9c326-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c326-114">属性</span><span class="sxs-lookup"><span data-stu-id="9c326-114">Attributes</span></span>

|<span data-ttu-id="9c326-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="9c326-115">**Attribute**</span></span>|<span data-ttu-id="9c326-116">**型**</span><span class="sxs-lookup"><span data-stu-id="9c326-116">**Type**</span></span>|<span data-ttu-id="9c326-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="9c326-117">**Required**</span></span>|<span data-ttu-id="9c326-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="9c326-118">**Description**</span></span>|<span data-ttu-id="9c326-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9c326-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c326-120">IX</span><span class="sxs-lookup"><span data-stu-id="9c326-120">IX</span></span>  <br/> |<span data-ttu-id="9c326-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="9c326-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c326-122">必須</span><span class="sxs-lookup"><span data-stu-id="9c326-122">required</span></span>  <br/> ||<span data-ttu-id="9c326-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="9c326-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

