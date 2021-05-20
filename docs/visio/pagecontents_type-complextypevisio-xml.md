---
title: PageContents_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: 067ec4376d65e1b5dfb9b431f4d2b6323b2e2bbf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537963"
---
# <a name="pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="b6938-102">PageContents_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b6938-102">PageContents_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b6938-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b6938-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6938-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b6938-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b6938-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b6938-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b6938-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b6938-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b6938-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b6938-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b6938-108">なし</span><span class="sxs-lookup"><span data-stu-id="b6938-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b6938-109">定義</span><span class="sxs-lookup"><span data-stu-id="b6938-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b6938-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b6938-110">Elements and attributes</span></span>

<span data-ttu-id="b6938-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6938-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b6938-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b6938-112">Child elements</span></span>

|<span data-ttu-id="b6938-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6938-113">**Element**</span></span>|<span data-ttu-id="b6938-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b6938-114">**Type**</span></span>|<span data-ttu-id="b6938-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b6938-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b6938-116">Connects</span><span class="sxs-lookup"><span data-stu-id="b6938-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b6938-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="b6938-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b6938-118">図形</span><span class="sxs-lookup"><span data-stu-id="b6938-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b6938-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="b6938-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b6938-120">属性</span><span class="sxs-lookup"><span data-stu-id="b6938-120">Attributes</span></span>

<span data-ttu-id="b6938-121">なし。</span><span class="sxs-lookup"><span data-stu-id="b6938-121">None.</span></span>
  

