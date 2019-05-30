---
title: Solution_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e41f5028-7173-986e-d381-5c02d05e4407
ms.openlocfilehash: cab57f2c4628538865d599bf40450a329de85fb8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540253"
---
# <a name="solutiontype-complextype-visio-xml"></a><span data-ttu-id="02972-102">Solution_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="02972-102">Solution_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="02972-103">型情報</span><span class="sxs-lookup"><span data-stu-id="02972-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02972-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02972-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="02972-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="02972-105">**Schema file**</span></span> <br/> |<span data-ttu-id="02972-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="02972-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="02972-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="02972-107">**Extension base**</span></span> <br/> |<span data-ttu-id="02972-108">None</span><span class="sxs-lookup"><span data-stu-id="02972-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02972-109">定義</span><span class="sxs-lookup"><span data-stu-id="02972-109">Definition</span></span>

```XML
          <xs:complexType name="Solution_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02972-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="02972-110">Elements and attributes</span></span>

<span data-ttu-id="02972-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="02972-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="02972-112">子要素</span><span class="sxs-lookup"><span data-stu-id="02972-112">Child elements</span></span>

|<span data-ttu-id="02972-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="02972-113">**Element**</span></span>|<span data-ttu-id="02972-114">**型**</span><span class="sxs-lookup"><span data-stu-id="02972-114">**Type**</span></span>|<span data-ttu-id="02972-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="02972-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02972-116">Rel</span><span class="sxs-lookup"><span data-stu-id="02972-116">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02972-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="02972-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="02972-118">属性</span><span class="sxs-lookup"><span data-stu-id="02972-118">Attributes</span></span>

<span data-ttu-id="02972-119">なし。</span><span class="sxs-lookup"><span data-stu-id="02972-119">None.</span></span>
  

