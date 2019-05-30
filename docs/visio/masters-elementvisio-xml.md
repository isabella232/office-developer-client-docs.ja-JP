---
title: Masters 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: 文書のマスター要素を含みます。
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538054"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="27931-103">Masters 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="27931-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="27931-104">文書のマスター要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="27931-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27931-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="27931-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27931-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="27931-106">**Element type**</span></span> <br/> |[<span data-ttu-id="27931-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="27931-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="27931-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="27931-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="27931-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="27931-109">**Schema file**</span></span> <br/> |<span data-ttu-id="27931-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="27931-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="27931-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="27931-111">**Document parts**</span></span> <br/> |<span data-ttu-id="27931-112">masters</span><span class="sxs-lookup"><span data-stu-id="27931-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27931-113">定義</span><span class="sxs-lookup"><span data-stu-id="27931-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="27931-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="27931-114">Elements and attributes</span></span>

<span data-ttu-id="27931-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27931-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="27931-116">親要素</span><span class="sxs-lookup"><span data-stu-id="27931-116">Parent elements</span></span>

<span data-ttu-id="27931-117">なし。</span><span class="sxs-lookup"><span data-stu-id="27931-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27931-118">子要素</span><span class="sxs-lookup"><span data-stu-id="27931-118">Child elements</span></span>

|<span data-ttu-id="27931-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="27931-119">**Element**</span></span>|<span data-ttu-id="27931-120">**型**</span><span class="sxs-lookup"><span data-stu-id="27931-120">**Type**</span></span>|<span data-ttu-id="27931-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="27931-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27931-122">Master</span><span class="sxs-lookup"><span data-stu-id="27931-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="27931-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="27931-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="27931-124">文書のマスターシェイプを定義する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="27931-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="27931-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="27931-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="27931-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="27931-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="27931-127">図面で定義されているマスターシェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="27931-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="27931-128">属性</span><span class="sxs-lookup"><span data-stu-id="27931-128">Attributes</span></span>

<span data-ttu-id="27931-129">なし。</span><span class="sxs-lookup"><span data-stu-id="27931-129">None.</span></span>
  

