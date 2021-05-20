---
title: Paragraph_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: fd7c5233b89bc92ed449d3d8d2767daa23ea8071
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540596"
---
# <a name="paragraph_type-complextype-visio-xml"></a><span data-ttu-id="927dc-102">Paragraph_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="927dc-102">Paragraph_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="927dc-103">型情報</span><span class="sxs-lookup"><span data-stu-id="927dc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="927dc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="927dc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="927dc-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="927dc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="927dc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="927dc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="927dc-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="927dc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="927dc-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="927dc-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="927dc-109">定義</span><span class="sxs-lookup"><span data-stu-id="927dc-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="927dc-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="927dc-110">Elements and attributes</span></span>

<span data-ttu-id="927dc-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="927dc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="927dc-112">子要素</span><span class="sxs-lookup"><span data-stu-id="927dc-112">Child elements</span></span>

|<span data-ttu-id="927dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="927dc-113">**Element**</span></span>|<span data-ttu-id="927dc-114">**型**</span><span class="sxs-lookup"><span data-stu-id="927dc-114">**Type**</span></span>|<span data-ttu-id="927dc-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="927dc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="927dc-116">Row</span><span class="sxs-lookup"><span data-stu-id="927dc-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="927dc-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="927dc-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="927dc-118">属性</span><span class="sxs-lookup"><span data-stu-id="927dc-118">Attributes</span></span>

<span data-ttu-id="927dc-119">なし。</span><span class="sxs-lookup"><span data-stu-id="927dc-119">None.</span></span>
  

