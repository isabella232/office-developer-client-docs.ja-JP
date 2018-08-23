---
title: RowDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 4d751df50d4239263947a917cb16f2305cb06170
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806297"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="5166a-102">RowDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="5166a-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5166a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5166a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5166a-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="5166a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5166a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5166a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5166a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5166a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5166a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5166a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5166a-108">なし</span><span class="sxs-lookup"><span data-stu-id="5166a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5166a-109">定義</span><span class="sxs-lookup"><span data-stu-id="5166a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5166a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5166a-110">Elements and attributes</span></span>

<span data-ttu-id="5166a-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5166a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5166a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5166a-112">Child elements</span></span>

|<span data-ttu-id="5166a-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="5166a-113">**Element**</span></span>|<span data-ttu-id="5166a-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5166a-114">**Type**</span></span>|<span data-ttu-id="5166a-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5166a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5166a-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="5166a-116">CellDef</span></span>](http://msdn.microsoft.com/library/f94c8227-020a-f613-3715-96a5eaaf14fb%28Office.15%29.aspx) <br/> |[<span data-ttu-id="5166a-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="5166a-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5166a-118">属性</span><span class="sxs-lookup"><span data-stu-id="5166a-118">Attributes</span></span>

<span data-ttu-id="5166a-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5166a-119">None.</span></span>
  

