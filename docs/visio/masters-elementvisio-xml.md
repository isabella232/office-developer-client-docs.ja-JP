---
title: マスター要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: マスター シェイプを含むドキュメントの要素です。
ms.openlocfilehash: d40071c64dc454eeb92f8518f89ef4de8b3b0cb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805823"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="8158e-103">マスター要素 ' Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="8158e-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="8158e-104">マスター シェイプを含むドキュメントの要素です。</span><span class="sxs-lookup"><span data-stu-id="8158e-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8158e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8158e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8158e-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="8158e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8158e-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="8158e-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8158e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8158e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8158e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8158e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8158e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8158e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8158e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8158e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8158e-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="8158e-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8158e-113">定義</span><span class="sxs-lookup"><span data-stu-id="8158e-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8158e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8158e-114">Elements and attributes</span></span>

<span data-ttu-id="8158e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8158e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8158e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8158e-116">Parent elements</span></span>

<span data-ttu-id="8158e-117">なし。</span><span class="sxs-lookup"><span data-stu-id="8158e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8158e-118">子要素</span><span class="sxs-lookup"><span data-stu-id="8158e-118">Child elements</span></span>

|<span data-ttu-id="8158e-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="8158e-119">**Element**</span></span>|<span data-ttu-id="8158e-120">**型**</span><span class="sxs-lookup"><span data-stu-id="8158e-120">**Type**</span></span>|<span data-ttu-id="8158e-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="8158e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8158e-122">Master</span><span class="sxs-lookup"><span data-stu-id="8158e-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8158e-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="8158e-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8158e-124">ドキュメントのマスターを定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8158e-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="8158e-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="8158e-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8158e-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="8158e-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8158e-127">ドキュメントで定義されているマスター シェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="8158e-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8158e-128">属性</span><span class="sxs-lookup"><span data-stu-id="8158e-128">Attributes</span></span>

<span data-ttu-id="8158e-129">なし。</span><span class="sxs-lookup"><span data-stu-id="8158e-129">None.</span></span>
  

