---
title: Solutions_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: b68955d2ed161d1ec0952b4a1b9d657fe0de81fc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540232"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="86d2c-102">Solutions_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="86d2c-102">Solutions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="86d2c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="86d2c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86d2c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="86d2c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="86d2c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="86d2c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="86d2c-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="86d2c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="86d2c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="86d2c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="86d2c-108">None</span><span class="sxs-lookup"><span data-stu-id="86d2c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86d2c-109">定義</span><span class="sxs-lookup"><span data-stu-id="86d2c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="86d2c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="86d2c-110">Elements and attributes</span></span>

<span data-ttu-id="86d2c-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86d2c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="86d2c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="86d2c-112">Child elements</span></span>

|<span data-ttu-id="86d2c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="86d2c-113">**Element**</span></span>|<span data-ttu-id="86d2c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="86d2c-114">**Type**</span></span>|<span data-ttu-id="86d2c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="86d2c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86d2c-116">Solution</span><span class="sxs-lookup"><span data-stu-id="86d2c-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86d2c-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="86d2c-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="86d2c-118">属性</span><span class="sxs-lookup"><span data-stu-id="86d2c-118">Attributes</span></span>

<span data-ttu-id="86d2c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="86d2c-119">None.</span></span>
  

