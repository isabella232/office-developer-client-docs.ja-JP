---
title: InfiniteLine_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4463d388-f5dd-4c43-71d4-82ba216d8d39
ms.openlocfilehash: ec0fb78e01afe0d16d959e100a93d053f96bc559
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542416"
---
# <a name="infinitelinetype-complextype-visio-xml"></a><span data-ttu-id="33042-102">InfiniteLine_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="33042-102">InfiniteLine_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="33042-103">型情報</span><span class="sxs-lookup"><span data-stu-id="33042-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33042-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="33042-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="33042-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="33042-105">**Schema file**</span></span> <br/> |<span data-ttu-id="33042-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="33042-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="33042-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="33042-107">**Extension base**</span></span> <br/> |<span data-ttu-id="33042-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="33042-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="33042-109">定義</span><span class="sxs-lookup"><span data-stu-id="33042-109">Definition</span></span>

```XML
          <xs:complexType name="InfiniteLine_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="33042-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="33042-110">Elements and attributes</span></span>

<span data-ttu-id="33042-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="33042-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="33042-112">子要素</span><span class="sxs-lookup"><span data-stu-id="33042-112">Child elements</span></span>

|<span data-ttu-id="33042-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="33042-113">**Element**</span></span>|<span data-ttu-id="33042-114">**型**</span><span class="sxs-lookup"><span data-stu-id="33042-114">**Type**</span></span>|<span data-ttu-id="33042-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="33042-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="33042-116">Cell</span><span class="sxs-lookup"><span data-stu-id="33042-116">Cell</span></span>](cell-element-infiniteline-rowvisio-xml.md) <br/> |[<span data-ttu-id="33042-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="33042-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="33042-118">属性</span><span class="sxs-lookup"><span data-stu-id="33042-118">Attributes</span></span>

<span data-ttu-id="33042-119">なし。</span><span class="sxs-lookup"><span data-stu-id="33042-119">None.</span></span>
  

