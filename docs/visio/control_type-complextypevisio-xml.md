---
title: Control_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eba241a-e64d-6bac-6d8e-a049e4febe96
ms.openlocfilehash: 8e5cb58e6964f2bb6db530e9ff01781520d06539
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538705"
---
# <a name="controltype-complextype-visio-xml"></a><span data-ttu-id="19aae-102">Control_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="19aae-102">Control_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="19aae-103">型情報</span><span class="sxs-lookup"><span data-stu-id="19aae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19aae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19aae-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19aae-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="19aae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19aae-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="19aae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19aae-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="19aae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19aae-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="19aae-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19aae-109">定義</span><span class="sxs-lookup"><span data-stu-id="19aae-109">Definition</span></span>

```XML
          <xs:complexType name="Control_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ControlRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="19aae-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="19aae-110">Elements and attributes</span></span>

<span data-ttu-id="19aae-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="19aae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19aae-112">子要素</span><span class="sxs-lookup"><span data-stu-id="19aae-112">Child elements</span></span>

|<span data-ttu-id="19aae-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="19aae-113">**Element**</span></span>|<span data-ttu-id="19aae-114">**型**</span><span class="sxs-lookup"><span data-stu-id="19aae-114">**Type**</span></span>|<span data-ttu-id="19aae-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="19aae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19aae-116">Row</span><span class="sxs-lookup"><span data-stu-id="19aae-116">Row</span></span>](row-element-controls-sectionvisio-xml.md) <br/> |[<span data-ttu-id="19aae-117">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="19aae-117">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="19aae-118">属性</span><span class="sxs-lookup"><span data-stu-id="19aae-118">Attributes</span></span>

<span data-ttu-id="19aae-119">なし。</span><span class="sxs-lookup"><span data-stu-id="19aae-119">None.</span></span>
  

