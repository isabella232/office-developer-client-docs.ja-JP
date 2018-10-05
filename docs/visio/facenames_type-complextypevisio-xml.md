---
title: FaceNames_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 6f9cd84dffc22f4211a8445a2d493ef7d4f4a4f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387147"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="84ea3-102">FaceNames_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="84ea3-102">FaceNames_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="84ea3-103">型情報</span><span class="sxs-lookup"><span data-stu-id="84ea3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84ea3-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="84ea3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="84ea3-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="84ea3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="84ea3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="84ea3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="84ea3-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="84ea3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="84ea3-108">なし</span><span class="sxs-lookup"><span data-stu-id="84ea3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="84ea3-109">定義</span><span class="sxs-lookup"><span data-stu-id="84ea3-109">Definition</span></span>

```XML
          <xs:complexType name="FaceNames_Type">
          
          <xs:sequence>
    <xs:element name="FaceName"  type="FaceName_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="84ea3-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="84ea3-110">Elements and attributes</span></span>

<span data-ttu-id="84ea3-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84ea3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="84ea3-112">子要素</span><span class="sxs-lookup"><span data-stu-id="84ea3-112">Child elements</span></span>

|<span data-ttu-id="84ea3-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="84ea3-113">**Element**</span></span>|<span data-ttu-id="84ea3-114">**型**</span><span class="sxs-lookup"><span data-stu-id="84ea3-114">**Type**</span></span>|<span data-ttu-id="84ea3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="84ea3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="84ea3-116">フォント名</span><span class="sxs-lookup"><span data-stu-id="84ea3-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="84ea3-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="84ea3-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="84ea3-118">属性</span><span class="sxs-lookup"><span data-stu-id="84ea3-118">Attributes</span></span>

<span data-ttu-id="84ea3-119">なし。</span><span class="sxs-lookup"><span data-stu-id="84ea3-119">None.</span></span>
  

