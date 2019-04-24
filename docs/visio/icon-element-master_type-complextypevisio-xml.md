---
title: Icon 要素 (Master_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80061e7d-dbcb-f7a1-b63a-052eee4ec7d7
description: ドキュメントのマスター要素に対して、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。
ms.openlocfilehash: 80d9089442318c834a9a211941187588359f7041
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344855"
---
# <a name="icon-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="9c159-103">Icon 要素 (Master_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9c159-103">Icon element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9c159-104">ドキュメントのマスター要素に対して、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c159-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a Master element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c159-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9c159-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c159-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9c159-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9c159-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="9c159-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9c159-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c159-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9c159-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9c159-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9c159-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="9c159-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9c159-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9c159-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9c159-112">masters</span><span class="sxs-lookup"><span data-stu-id="9c159-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c159-113">定義</span><span class="sxs-lookup"><span data-stu-id="9c159-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c159-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9c159-114">Elements and attributes</span></span>

<span data-ttu-id="9c159-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c159-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9c159-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9c159-116">Parent elements</span></span>

|<span data-ttu-id="9c159-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9c159-117">**Element**</span></span>|<span data-ttu-id="9c159-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9c159-118">**Type**</span></span>|<span data-ttu-id="9c159-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9c159-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c159-120">Master</span><span class="sxs-lookup"><span data-stu-id="9c159-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c159-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="9c159-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c159-122">図面のマスターシェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c159-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c159-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9c159-123">Child elements</span></span>

<span data-ttu-id="9c159-124">なし。</span><span class="sxs-lookup"><span data-stu-id="9c159-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c159-125">属性</span><span class="sxs-lookup"><span data-stu-id="9c159-125">Attributes</span></span>

<span data-ttu-id="9c159-126">なし。</span><span class="sxs-lookup"><span data-stu-id="9c159-126">None.</span></span>
  

