---
title: Paragraph_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: 8a57a0df516f998e4e815240f1405962e11f848d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338809"
---
# <a name="paragraphtype-complextype-visio-xml"></a><span data-ttu-id="56e8c-102">Paragraph_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="56e8c-102">Paragraph_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="56e8c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="56e8c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56e8c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="56e8c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="56e8c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="56e8c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="56e8c-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="56e8c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="56e8c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="56e8c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="56e8c-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="56e8c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56e8c-109">定義</span><span class="sxs-lookup"><span data-stu-id="56e8c-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="56e8c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="56e8c-110">Elements and attributes</span></span>

<span data-ttu-id="56e8c-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="56e8c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="56e8c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="56e8c-112">Child elements</span></span>

|<span data-ttu-id="56e8c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="56e8c-113">**Element**</span></span>|<span data-ttu-id="56e8c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="56e8c-114">**Type**</span></span>|<span data-ttu-id="56e8c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="56e8c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56e8c-116">Row</span><span class="sxs-lookup"><span data-stu-id="56e8c-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="56e8c-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="56e8c-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="56e8c-118">属性</span><span class="sxs-lookup"><span data-stu-id="56e8c-118">Attributes</span></span>

<span data-ttu-id="56e8c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="56e8c-119">None.</span></span>
  

