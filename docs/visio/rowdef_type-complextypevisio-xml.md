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
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="b6cab-102">RowDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b6cab-102">RowDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b6cab-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b6cab-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6cab-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b6cab-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b6cab-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b6cab-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b6cab-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="b6cab-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b6cab-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b6cab-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b6cab-108">None</span><span class="sxs-lookup"><span data-stu-id="b6cab-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b6cab-109">定義</span><span class="sxs-lookup"><span data-stu-id="b6cab-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b6cab-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b6cab-110">Elements and attributes</span></span>

<span data-ttu-id="b6cab-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6cab-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b6cab-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b6cab-112">Child elements</span></span>

|<span data-ttu-id="b6cab-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6cab-113">**Element**</span></span>|<span data-ttu-id="b6cab-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b6cab-114">**Type**</span></span>|<span data-ttu-id="b6cab-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b6cab-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6cab-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="b6cab-116">CellDef</span></span> <br/> |[<span data-ttu-id="b6cab-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="b6cab-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b6cab-118">属性</span><span class="sxs-lookup"><span data-stu-id="b6cab-118">Attributes</span></span>

<span data-ttu-id="b6cab-119">なし。</span><span class="sxs-lookup"><span data-stu-id="b6cab-119">None.</span></span>
  

