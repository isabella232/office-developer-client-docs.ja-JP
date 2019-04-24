---
title: StyleSheets_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 1992f0e31ae972320f80f99d94164fbd1dbc6d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346782"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="78787-102">StyleSheets_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="78787-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="78787-103">型情報</span><span class="sxs-lookup"><span data-stu-id="78787-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78787-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="78787-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="78787-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="78787-105">**Schema file**</span></span> <br/> |<span data-ttu-id="78787-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="78787-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="78787-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="78787-107">**Extension base**</span></span> <br/> |<span data-ttu-id="78787-108">なし</span><span class="sxs-lookup"><span data-stu-id="78787-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78787-109">定義</span><span class="sxs-lookup"><span data-stu-id="78787-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="78787-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="78787-110">Elements and attributes</span></span>

<span data-ttu-id="78787-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="78787-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="78787-112">子要素</span><span class="sxs-lookup"><span data-stu-id="78787-112">Child elements</span></span>

|<span data-ttu-id="78787-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="78787-113">**Element**</span></span>|<span data-ttu-id="78787-114">**型**</span><span class="sxs-lookup"><span data-stu-id="78787-114">**Type**</span></span>|<span data-ttu-id="78787-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="78787-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78787-116">xsl</span><span class="sxs-lookup"><span data-stu-id="78787-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78787-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="78787-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="78787-118">属性</span><span class="sxs-lookup"><span data-stu-id="78787-118">Attributes</span></span>

<span data-ttu-id="78787-119">なし。</span><span class="sxs-lookup"><span data-stu-id="78787-119">None.</span></span>
  

