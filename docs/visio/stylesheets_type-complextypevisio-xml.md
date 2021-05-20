---
title: StyleSheets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 845580f2842c098cfb16776b9ab1d5d513ef8e22
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538887"
---
# <a name="stylesheets_type-complextype-visio-xml"></a><span data-ttu-id="bbad5-102">StyleSheets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bbad5-102">StyleSheets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bbad5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="bbad5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbad5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bbad5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bbad5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bbad5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bbad5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bbad5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bbad5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="bbad5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bbad5-108">なし</span><span class="sxs-lookup"><span data-stu-id="bbad5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bbad5-109">定義</span><span class="sxs-lookup"><span data-stu-id="bbad5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bbad5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bbad5-110">Elements and attributes</span></span>

<span data-ttu-id="bbad5-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbad5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bbad5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bbad5-112">Child elements</span></span>

|<span data-ttu-id="bbad5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bbad5-113">**Element**</span></span>|<span data-ttu-id="bbad5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="bbad5-114">**Type**</span></span>|<span data-ttu-id="bbad5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="bbad5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bbad5-116">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="bbad5-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bbad5-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="bbad5-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bbad5-118">属性</span><span class="sxs-lookup"><span data-stu-id="bbad5-118">Attributes</span></span>

<span data-ttu-id="bbad5-119">なし。</span><span class="sxs-lookup"><span data-stu-id="bbad5-119">None.</span></span>
  

