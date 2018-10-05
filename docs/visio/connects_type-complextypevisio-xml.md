---
title: Connects_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: ed5046656554fdd64251601c12e6817d586cd689
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399880"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="693fe-102">Connects_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="693fe-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="693fe-103">型情報</span><span class="sxs-lookup"><span data-stu-id="693fe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="693fe-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="693fe-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="693fe-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="693fe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="693fe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="693fe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="693fe-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="693fe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="693fe-108">なし</span><span class="sxs-lookup"><span data-stu-id="693fe-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="693fe-109">定義</span><span class="sxs-lookup"><span data-stu-id="693fe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="693fe-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="693fe-110">Elements and attributes</span></span>

<span data-ttu-id="693fe-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="693fe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="693fe-112">子要素</span><span class="sxs-lookup"><span data-stu-id="693fe-112">Child elements</span></span>

|<span data-ttu-id="693fe-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="693fe-113">**Element**</span></span>|<span data-ttu-id="693fe-114">**型**</span><span class="sxs-lookup"><span data-stu-id="693fe-114">**Type**</span></span>|<span data-ttu-id="693fe-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="693fe-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="693fe-116">Connect</span><span class="sxs-lookup"><span data-stu-id="693fe-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="693fe-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="693fe-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="693fe-118">属性</span><span class="sxs-lookup"><span data-stu-id="693fe-118">Attributes</span></span>

<span data-ttu-id="693fe-119">なし。</span><span class="sxs-lookup"><span data-stu-id="693fe-119">None.</span></span>
  

