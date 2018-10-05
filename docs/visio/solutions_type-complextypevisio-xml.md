---
title: Solutions_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: bf43b971399ec69c6f73cbfaaa6cade8c583d3c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400538"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="bda5d-102">Solutions_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="bda5d-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bda5d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="bda5d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bda5d-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="bda5d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bda5d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bda5d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bda5d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bda5d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bda5d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="bda5d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bda5d-108">なし</span><span class="sxs-lookup"><span data-stu-id="bda5d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bda5d-109">定義</span><span class="sxs-lookup"><span data-stu-id="bda5d-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bda5d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bda5d-110">Elements and attributes</span></span>

<span data-ttu-id="bda5d-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bda5d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bda5d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bda5d-112">Child elements</span></span>

|<span data-ttu-id="bda5d-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="bda5d-113">**Element**</span></span>|<span data-ttu-id="bda5d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="bda5d-114">**Type**</span></span>|<span data-ttu-id="bda5d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="bda5d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bda5d-116">Solution</span><span class="sxs-lookup"><span data-stu-id="bda5d-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bda5d-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="bda5d-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bda5d-118">属性</span><span class="sxs-lookup"><span data-stu-id="bda5d-118">Attributes</span></span>

<span data-ttu-id="bda5d-119">なし。</span><span class="sxs-lookup"><span data-stu-id="bda5d-119">None.</span></span>
  

