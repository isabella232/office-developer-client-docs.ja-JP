---
title: HeaderMargin_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 70b16680446af8973605d24f41b69778a1ec2c2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805525"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="1eb3c-102">HeaderMargin_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1eb3c-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1eb3c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1eb3c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1eb3c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1eb3c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1eb3c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1eb3c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1eb3c-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1eb3c-108">xsd:double</span><span class="sxs-lookup"><span data-stu-id="1eb3c-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1eb3c-109">定義</span><span class="sxs-lookup"><span data-stu-id="1eb3c-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1eb3c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1eb3c-110">Elements and attributes</span></span>

<span data-ttu-id="1eb3c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1eb3c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1eb3c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1eb3c-112">Child elements</span></span>

<span data-ttu-id="1eb3c-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1eb3c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1eb3c-114">属性</span><span class="sxs-lookup"><span data-stu-id="1eb3c-114">Attributes</span></span>

|<span data-ttu-id="1eb3c-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-115">**Attribute**</span></span>|<span data-ttu-id="1eb3c-116">**型**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-116">**Type**</span></span>|<span data-ttu-id="1eb3c-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-117">**Required**</span></span>|<span data-ttu-id="1eb3c-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-118">**Description**</span></span>|<span data-ttu-id="1eb3c-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1eb3c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1eb3c-120">種類</span><span class="sxs-lookup"><span data-stu-id="1eb3c-120">Unit</span></span>  <br/> |<span data-ttu-id="1eb3c-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1eb3c-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1eb3c-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="1eb3c-122">optional</span></span>  <br/> ||<span data-ttu-id="1eb3c-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1eb3c-123">Values of the xsd:string type.</span></span>  <br/> |
   

