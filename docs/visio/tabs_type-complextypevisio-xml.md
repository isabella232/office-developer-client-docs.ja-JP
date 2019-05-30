---
title: Tabs_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b97155ce-f0d2-e35c-bc58-e288f653ce2c
ms.openlocfilehash: f3c484fe8656d97484dd136175506bf60f0e299b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538845"
---
# <a name="tabstype-complextype-visio-xml"></a><span data-ttu-id="aabff-102">Tabs_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aabff-102">Tabs_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="aabff-103">型情報</span><span class="sxs-lookup"><span data-stu-id="aabff-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aabff-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aabff-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aabff-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="aabff-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aabff-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="aabff-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aabff-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="aabff-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aabff-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="aabff-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aabff-109">定義</span><span class="sxs-lookup"><span data-stu-id="aabff-109">Definition</span></span>

```XML
          <xs:complexType name="Tabs_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="TabsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aabff-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="aabff-110">Elements and attributes</span></span>

<span data-ttu-id="aabff-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aabff-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aabff-112">子要素</span><span class="sxs-lookup"><span data-stu-id="aabff-112">Child elements</span></span>

|<span data-ttu-id="aabff-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="aabff-113">**Element**</span></span>|<span data-ttu-id="aabff-114">**型**</span><span class="sxs-lookup"><span data-stu-id="aabff-114">**Type**</span></span>|<span data-ttu-id="aabff-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="aabff-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aabff-116">Row</span><span class="sxs-lookup"><span data-stu-id="aabff-116">Row</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="aabff-117">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="aabff-117">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aabff-118">属性</span><span class="sxs-lookup"><span data-stu-id="aabff-118">Attributes</span></span>

<span data-ttu-id="aabff-119">なし。</span><span class="sxs-lookup"><span data-stu-id="aabff-119">None.</span></span>
  

