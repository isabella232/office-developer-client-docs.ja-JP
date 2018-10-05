---
title: FillGradient_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82545cdc-890d-1b2f-9c8f-4740f32d0ed7
ms.openlocfilehash: 6ae61b730a59c5f8e6acae3b7a4c5cb8e0298f91
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388743"
---
# <a name="fillgradienttype-complextype-visio-xml"></a><span data-ttu-id="88fb5-102">FillGradient_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="88fb5-102">FillGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88fb5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="88fb5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88fb5-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="88fb5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88fb5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88fb5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88fb5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88fb5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88fb5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="88fb5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88fb5-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="88fb5-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88fb5-109">定義</span><span class="sxs-lookup"><span data-stu-id="88fb5-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FillGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88fb5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88fb5-110">Elements and attributes</span></span>

<span data-ttu-id="88fb5-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88fb5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88fb5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="88fb5-112">Child elements</span></span>

|<span data-ttu-id="88fb5-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="88fb5-113">**Element**</span></span>|<span data-ttu-id="88fb5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="88fb5-114">**Type**</span></span>|<span data-ttu-id="88fb5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="88fb5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88fb5-116">Row</span><span class="sxs-lookup"><span data-stu-id="88fb5-116">Row</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="88fb5-117">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="88fb5-117">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="88fb5-118">属性</span><span class="sxs-lookup"><span data-stu-id="88fb5-118">Attributes</span></span>

<span data-ttu-id="88fb5-119">なし。</span><span class="sxs-lookup"><span data-stu-id="88fb5-119">None.</span></span>
  

