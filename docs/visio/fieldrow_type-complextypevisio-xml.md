---
title: FieldRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: f6102c89cc0e484b1a07fb11bf26285df8954a5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542360"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="a5448-102">FieldRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a5448-102">FieldRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a5448-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a5448-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5448-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a5448-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a5448-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a5448-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a5448-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="a5448-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a5448-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a5448-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a5448-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="a5448-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a5448-109">定義</span><span class="sxs-lookup"><span data-stu-id="a5448-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="a5448-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a5448-110">Elements and attributes</span></span>

<span data-ttu-id="a5448-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5448-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a5448-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a5448-112">Child elements</span></span>

|<span data-ttu-id="a5448-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5448-113">**Element**</span></span>|<span data-ttu-id="a5448-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a5448-114">**Type**</span></span>|<span data-ttu-id="a5448-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a5448-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a5448-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a5448-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a5448-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a5448-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a5448-118">属性</span><span class="sxs-lookup"><span data-stu-id="a5448-118">Attributes</span></span>

<span data-ttu-id="a5448-119">なし。</span><span class="sxs-lookup"><span data-stu-id="a5448-119">None.</span></span>
  

