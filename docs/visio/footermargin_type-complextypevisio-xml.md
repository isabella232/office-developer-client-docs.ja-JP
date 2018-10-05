---
title: FooterMargin_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398935"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="6f7d4-102">FooterMargin_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6f7d4-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6f7d4-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6f7d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f7d4-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6f7d4-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6f7d4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6f7d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6f7d4-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6f7d4-108">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6f7d4-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f7d4-109">定義</span><span class="sxs-lookup"><span data-stu-id="6f7d4-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6f7d4-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6f7d4-110">Elements and attributes</span></span>

<span data-ttu-id="6f7d4-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6f7d4-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6f7d4-112">Child elements</span></span>

<span data-ttu-id="6f7d4-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f7d4-114">属性</span><span class="sxs-lookup"><span data-stu-id="6f7d4-114">Attributes</span></span>

|<span data-ttu-id="6f7d4-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-115">**Attribute**</span></span>|<span data-ttu-id="6f7d4-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-116">**Type**</span></span>|<span data-ttu-id="6f7d4-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-117">**Required**</span></span>|<span data-ttu-id="6f7d4-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-118">**Description**</span></span>|<span data-ttu-id="6f7d4-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6f7d4-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6f7d4-120">種類</span><span class="sxs-lookup"><span data-stu-id="6f7d4-120">Unit</span></span>  <br/> |<span data-ttu-id="6f7d4-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6f7d4-121">xsd:string</span></span>  <br/> |<span data-ttu-id="6f7d4-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="6f7d4-122">optional</span></span>  <br/> ||<span data-ttu-id="6f7d4-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-123">Values of the xsd:string type.</span></span>  <br/> |
   

