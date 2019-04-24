---
title: SnapAngles_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1110a656-d8cd-19d0-1af0-31a6675bf89b
ms.openlocfilehash: 4f48934d436fd0830019898cb6d24e940937f539
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334623"
---
# <a name="snapanglestype-complextype-visio-xml"></a><span data-ttu-id="fc60c-102">SnapAngles_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="fc60c-102">SnapAngles_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fc60c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="fc60c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc60c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc60c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fc60c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fc60c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fc60c-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="fc60c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fc60c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="fc60c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fc60c-108">なし</span><span class="sxs-lookup"><span data-stu-id="fc60c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc60c-109">定義</span><span class="sxs-lookup"><span data-stu-id="fc60c-109">Definition</span></span>

```XML
          <xs:complexType name="SnapAngles_Type">
          
          <xs:sequence>
    <xs:element name="SnapAngle"  type="SnapAngle_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc60c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fc60c-110">Elements and attributes</span></span>

<span data-ttu-id="fc60c-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc60c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fc60c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="fc60c-112">Child elements</span></span>

|<span data-ttu-id="fc60c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc60c-113">**Element**</span></span>|<span data-ttu-id="fc60c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="fc60c-114">**Type**</span></span>|<span data-ttu-id="fc60c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="fc60c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc60c-116">snapangle</span><span class="sxs-lookup"><span data-stu-id="fc60c-116">SnapAngle</span></span>](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fc60c-117">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="fc60c-117">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fc60c-118">属性</span><span class="sxs-lookup"><span data-stu-id="fc60c-118">Attributes</span></span>

<span data-ttu-id="fc60c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="fc60c-119">None.</span></span>
  

