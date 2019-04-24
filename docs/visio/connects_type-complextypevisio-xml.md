---
title: Connects_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: ed5046656554fdd64251601c12e6817d586cd689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319573"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="5fe11-102">Connects_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5fe11-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5fe11-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5fe11-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fe11-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5fe11-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5fe11-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5fe11-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5fe11-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="5fe11-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5fe11-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5fe11-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5fe11-108">なし</span><span class="sxs-lookup"><span data-stu-id="5fe11-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5fe11-109">定義</span><span class="sxs-lookup"><span data-stu-id="5fe11-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5fe11-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5fe11-110">Elements and attributes</span></span>

<span data-ttu-id="5fe11-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fe11-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5fe11-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5fe11-112">Child elements</span></span>

|<span data-ttu-id="5fe11-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fe11-113">**Element**</span></span>|<span data-ttu-id="5fe11-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5fe11-114">**Type**</span></span>|<span data-ttu-id="5fe11-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5fe11-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5fe11-116">Connect</span><span class="sxs-lookup"><span data-stu-id="5fe11-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5fe11-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="5fe11-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5fe11-118">属性</span><span class="sxs-lookup"><span data-stu-id="5fe11-118">Attributes</span></span>

<span data-ttu-id="5fe11-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5fe11-119">None.</span></span>
  

