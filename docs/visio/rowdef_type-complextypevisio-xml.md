---
title: RowDef_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 11acab820fe51b6dde9cf9d57977699ca3c977cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355770"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="6c711-102">RowDef_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6c711-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6c711-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6c711-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c711-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c711-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6c711-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6c711-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6c711-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="6c711-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6c711-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6c711-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6c711-108">なし</span><span class="sxs-lookup"><span data-stu-id="6c711-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c711-109">定義</span><span class="sxs-lookup"><span data-stu-id="6c711-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6c711-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6c711-110">Elements and attributes</span></span>

<span data-ttu-id="6c711-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c711-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6c711-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6c711-112">Child elements</span></span>

|<span data-ttu-id="6c711-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c711-113">**Element**</span></span>|<span data-ttu-id="6c711-114">**型**</span><span class="sxs-lookup"><span data-stu-id="6c711-114">**Type**</span></span>|<span data-ttu-id="6c711-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="6c711-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c711-116">celldef</span><span class="sxs-lookup"><span data-stu-id="6c711-116">CellDef</span></span> <br/> |[<span data-ttu-id="6c711-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="6c711-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6c711-118">属性</span><span class="sxs-lookup"><span data-stu-id="6c711-118">Attributes</span></span>

<span data-ttu-id="6c711-119">なし。</span><span class="sxs-lookup"><span data-stu-id="6c711-119">None.</span></span>
  

