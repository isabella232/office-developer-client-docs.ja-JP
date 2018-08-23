---
title: Connects_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: 4d2740bc0ee0934b28bbebbc10ca9c861c563be0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805100"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="668e1-102">Connects_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="668e1-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="668e1-103">型情報</span><span class="sxs-lookup"><span data-stu-id="668e1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="668e1-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="668e1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="668e1-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="668e1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="668e1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="668e1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="668e1-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="668e1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="668e1-108">なし</span><span class="sxs-lookup"><span data-stu-id="668e1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="668e1-109">定義</span><span class="sxs-lookup"><span data-stu-id="668e1-109">Definition</span></span>

```XML
          <xs:complexType name="Connects_Type">
          
          <xs:sequence>
    <xs:element name="Connect"  type="Connect_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="668e1-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="668e1-110">Elements and attributes</span></span>

<span data-ttu-id="668e1-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="668e1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="668e1-112">子要素</span><span class="sxs-lookup"><span data-stu-id="668e1-112">Child elements</span></span>

|<span data-ttu-id="668e1-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="668e1-113">**Element**</span></span>|<span data-ttu-id="668e1-114">**型**</span><span class="sxs-lookup"><span data-stu-id="668e1-114">**Type**</span></span>|<span data-ttu-id="668e1-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="668e1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="668e1-116">Connect</span><span class="sxs-lookup"><span data-stu-id="668e1-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="668e1-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="668e1-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="668e1-118">属性</span><span class="sxs-lookup"><span data-stu-id="668e1-118">Attributes</span></span>

<span data-ttu-id="668e1-119">なし。</span><span class="sxs-lookup"><span data-stu-id="668e1-119">None.</span></span>
  

