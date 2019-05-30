---
title: LineGradient_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 6be5575336b3fb3ae014abd2685733ce4889f841
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541170"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="5b5d5-102">LineGradient_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5b5d5-102">LineGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5b5d5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5b5d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b5d5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b5d5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5b5d5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5b5d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5b5d5-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="5b5d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5b5d5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5b5d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5b5d5-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5b5d5-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b5d5-109">定義</span><span class="sxs-lookup"><span data-stu-id="5b5d5-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b5d5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5b5d5-110">Elements and attributes</span></span>

<span data-ttu-id="5b5d5-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b5d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5b5d5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5b5d5-112">Child elements</span></span>

|<span data-ttu-id="5b5d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b5d5-113">**Element**</span></span>|<span data-ttu-id="5b5d5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5b5d5-114">**Type**</span></span>|<span data-ttu-id="5b5d5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b5d5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b5d5-116">Row</span><span class="sxs-lookup"><span data-stu-id="5b5d5-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5b5d5-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="5b5d5-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5b5d5-118">属性</span><span class="sxs-lookup"><span data-stu-id="5b5d5-118">Attributes</span></span>

<span data-ttu-id="5b5d5-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5b5d5-119">None.</span></span>
  

