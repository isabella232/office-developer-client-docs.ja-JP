---
title: Layer_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f92ac1cc-fad2-dab9-5507-838c006ed633
ms.openlocfilehash: 1614a2eb8606144d28fc0422d9fc2c44c48910d1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541289"
---
# <a name="layertype-complextype-visio-xml"></a><span data-ttu-id="ce624-102">Layer_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ce624-102">Layer_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ce624-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ce624-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce624-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ce624-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ce624-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ce624-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ce624-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="ce624-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ce624-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="ce624-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ce624-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ce624-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ce624-109">定義</span><span class="sxs-lookup"><span data-stu-id="ce624-109">Definition</span></span>

```XML
          <xs:complexType name="Layer_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LayerRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ce624-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ce624-110">Elements and attributes</span></span>

<span data-ttu-id="ce624-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce624-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ce624-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ce624-112">Child elements</span></span>

|<span data-ttu-id="ce624-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce624-113">**Element**</span></span>|<span data-ttu-id="ce624-114">**型**</span><span class="sxs-lookup"><span data-stu-id="ce624-114">**Type**</span></span>|<span data-ttu-id="ce624-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ce624-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce624-116">Row</span><span class="sxs-lookup"><span data-stu-id="ce624-116">Row</span></span>](row-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ce624-117">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="ce624-117">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ce624-118">属性</span><span class="sxs-lookup"><span data-stu-id="ce624-118">Attributes</span></span>

<span data-ttu-id="ce624-119">なし。</span><span class="sxs-lookup"><span data-stu-id="ce624-119">None.</span></span>
  

