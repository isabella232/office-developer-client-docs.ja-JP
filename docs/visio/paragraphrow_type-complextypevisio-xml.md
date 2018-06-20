---
title: ParagraphRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32bb67e1-8db8-fe28-f173-028a20bb136c
ms.openlocfilehash: cec77978cf2f54e497f34a4619bea78f46402e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805988"
---
# <a name="paragraphrowtype-complextype-visio-xml"></a><span data-ttu-id="d296e-102">ParagraphRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d296e-102">ParagraphRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d296e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d296e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d296e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d296e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d296e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d296e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d296e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d296e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d296e-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="d296e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d296e-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="d296e-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d296e-109">定義</span><span class="sxs-lookup"><span data-stu-id="d296e-109">Definition</span></span>

```XML
          <xs:complexType name="ParagraphRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="d296e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d296e-110">Elements and attributes</span></span>

<span data-ttu-id="d296e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d296e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d296e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d296e-112">Child elements</span></span>

|<span data-ttu-id="d296e-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="d296e-113">**Element**</span></span>|<span data-ttu-id="d296e-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d296e-114">**Type**</span></span>|<span data-ttu-id="d296e-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d296e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d296e-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d296e-116">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d296e-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d296e-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d296e-118">属性</span><span class="sxs-lookup"><span data-stu-id="d296e-118">Attributes</span></span>

<span data-ttu-id="d296e-119">なし。</span><span class="sxs-lookup"><span data-stu-id="d296e-119">None.</span></span>
  

