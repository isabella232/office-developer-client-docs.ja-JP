---
title: PageContents_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: ab74c646e72a7ebe5fbf5863c196d5b115be9b43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805956"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="54ab9-102">PageContents_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="54ab9-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="54ab9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="54ab9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54ab9-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="54ab9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="54ab9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="54ab9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="54ab9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="54ab9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="54ab9-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="54ab9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="54ab9-108">なし</span><span class="sxs-lookup"><span data-stu-id="54ab9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54ab9-109">定義</span><span class="sxs-lookup"><span data-stu-id="54ab9-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54ab9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="54ab9-110">Elements and attributes</span></span>

<span data-ttu-id="54ab9-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="54ab9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="54ab9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="54ab9-112">Child elements</span></span>

|<span data-ttu-id="54ab9-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="54ab9-113">**Element**</span></span>|<span data-ttu-id="54ab9-114">**型**</span><span class="sxs-lookup"><span data-stu-id="54ab9-114">**Type**</span></span>|<span data-ttu-id="54ab9-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="54ab9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54ab9-116">接続</span><span class="sxs-lookup"><span data-stu-id="54ab9-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54ab9-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="54ab9-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="54ab9-118">Shapes</span><span class="sxs-lookup"><span data-stu-id="54ab9-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54ab9-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="54ab9-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="54ab9-120">属性</span><span class="sxs-lookup"><span data-stu-id="54ab9-120">Attributes</span></span>

<span data-ttu-id="54ab9-121">なし。</span><span class="sxs-lookup"><span data-stu-id="54ab9-121">None.</span></span>
  

