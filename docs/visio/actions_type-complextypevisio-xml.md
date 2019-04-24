---
title: Actions_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 158a0dfa31c2da3ac9e530c07edd075b4fabbd75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283052"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="114a0-102">Actions_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="114a0-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="114a0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="114a0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="114a0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="114a0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="114a0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="114a0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="114a0-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="114a0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="114a0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="114a0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="114a0-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="114a0-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="114a0-109">定義</span><span class="sxs-lookup"><span data-stu-id="114a0-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="114a0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="114a0-110">Elements and attributes</span></span>

<span data-ttu-id="114a0-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="114a0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="114a0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="114a0-112">Child elements</span></span>

|<span data-ttu-id="114a0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="114a0-113">**Element**</span></span>|<span data-ttu-id="114a0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="114a0-114">**Type**</span></span>|<span data-ttu-id="114a0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="114a0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="114a0-116">Row</span><span class="sxs-lookup"><span data-stu-id="114a0-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="114a0-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="114a0-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="114a0-118">属性</span><span class="sxs-lookup"><span data-stu-id="114a0-118">Attributes</span></span>

<span data-ttu-id="114a0-119">なし。</span><span class="sxs-lookup"><span data-stu-id="114a0-119">None.</span></span>
  

