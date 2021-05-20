---
title: ActionTag_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: 864f4f9b5069fa3968ceb8d3a8db1589113d931a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541415"
---
# <a name="actiontag_type-complextype-visio-xml"></a><span data-ttu-id="a411d-102">ActionTag_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a411d-102">ActionTag_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a411d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a411d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a411d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a411d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a411d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a411d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a411d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a411d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a411d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a411d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a411d-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a411d-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a411d-109">定義</span><span class="sxs-lookup"><span data-stu-id="a411d-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a411d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a411d-110">Elements and attributes</span></span>

<span data-ttu-id="a411d-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a411d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a411d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a411d-112">Child elements</span></span>

|<span data-ttu-id="a411d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a411d-113">**Element**</span></span>|<span data-ttu-id="a411d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a411d-114">**Type**</span></span>|<span data-ttu-id="a411d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a411d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a411d-116">Row</span><span class="sxs-lookup"><span data-stu-id="a411d-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a411d-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="a411d-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a411d-118">属性</span><span class="sxs-lookup"><span data-stu-id="a411d-118">Attributes</span></span>

<span data-ttu-id="a411d-119">なし。</span><span class="sxs-lookup"><span data-stu-id="a411d-119">None.</span></span>
  

