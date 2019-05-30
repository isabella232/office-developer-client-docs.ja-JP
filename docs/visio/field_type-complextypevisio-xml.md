---
title: Field_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c346fb8d-f247-4a14-19cd-9368ec86ce3f
ms.openlocfilehash: e67ea9dd5eed1892888ccd59c2ade1d95bd5d79e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542367"
---
# <a name="fieldtype-complextype-visio-xml"></a><span data-ttu-id="b490c-102">Field_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b490c-102">Field_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b490c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b490c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b490c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b490c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b490c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b490c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b490c-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="b490c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b490c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b490c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b490c-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b490c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b490c-109">定義</span><span class="sxs-lookup"><span data-stu-id="b490c-109">Definition</span></span>

```XML
          <xs:complexType name="Field_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FieldRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b490c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b490c-110">Elements and attributes</span></span>

<span data-ttu-id="b490c-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b490c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b490c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b490c-112">Child elements</span></span>

|<span data-ttu-id="b490c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b490c-113">**Element**</span></span>|<span data-ttu-id="b490c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b490c-114">**Type**</span></span>|<span data-ttu-id="b490c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b490c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b490c-116">Row</span><span class="sxs-lookup"><span data-stu-id="b490c-116">Row</span></span>](row-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b490c-117">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="b490c-117">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b490c-118">属性</span><span class="sxs-lookup"><span data-stu-id="b490c-118">Attributes</span></span>

<span data-ttu-id="b490c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="b490c-119">None.</span></span>
  

