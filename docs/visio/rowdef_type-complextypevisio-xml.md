---
title: RowDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 79a01d9fe5edf1de933f05683eca3bfd6e95e4b3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538138"
---
# <a name="rowdef_type-complextype-visio-xml"></a><span data-ttu-id="57a50-102">RowDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="57a50-102">RowDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="57a50-103">型情報</span><span class="sxs-lookup"><span data-stu-id="57a50-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57a50-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="57a50-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="57a50-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="57a50-105">**Schema file**</span></span> <br/> |<span data-ttu-id="57a50-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="57a50-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="57a50-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="57a50-107">**Extension base**</span></span> <br/> |<span data-ttu-id="57a50-108">なし</span><span class="sxs-lookup"><span data-stu-id="57a50-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57a50-109">定義</span><span class="sxs-lookup"><span data-stu-id="57a50-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="57a50-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="57a50-110">Elements and attributes</span></span>

<span data-ttu-id="57a50-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="57a50-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="57a50-112">子要素</span><span class="sxs-lookup"><span data-stu-id="57a50-112">Child elements</span></span>

|<span data-ttu-id="57a50-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="57a50-113">**Element**</span></span>|<span data-ttu-id="57a50-114">**型**</span><span class="sxs-lookup"><span data-stu-id="57a50-114">**Type**</span></span>|<span data-ttu-id="57a50-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="57a50-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57a50-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="57a50-116">CellDef</span></span> <br/> |[<span data-ttu-id="57a50-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="57a50-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="57a50-118">属性</span><span class="sxs-lookup"><span data-stu-id="57a50-118">Attributes</span></span>

<span data-ttu-id="57a50-119">なし。</span><span class="sxs-lookup"><span data-stu-id="57a50-119">None.</span></span>
  

