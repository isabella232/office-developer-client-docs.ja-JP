---
title: SnapAngles 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 803ddfc1-b7d3-736f-2d85-7b8780ef9278
description: SnapAngle 要素のコレクションを格納します。
ms.openlocfilehash: d0b2c2a0643b4f3bccd5b450ef0d9c89ce9ab7c2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540393"
---
# <a name="snapangles-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="5b008-103">SnapAngles 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5b008-103">SnapAngles element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5b008-104">**Snapangle**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="5b008-104">Contains a collection of **SnapAngle** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5b008-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5b008-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b008-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5b008-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5b008-107">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="5b008-107">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5b008-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b008-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5b008-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5b008-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5b008-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="5b008-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5b008-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5b008-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5b008-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="5b008-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b008-113">定義</span><span class="sxs-lookup"><span data-stu-id="5b008-113">Definition</span></span>

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b008-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5b008-114">Elements and attributes</span></span>

<span data-ttu-id="5b008-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b008-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5b008-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5b008-116">Parent elements</span></span>

|<span data-ttu-id="5b008-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5b008-117">**Element**</span></span>|<span data-ttu-id="5b008-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5b008-118">**Type**</span></span>|<span data-ttu-id="5b008-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b008-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b008-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="5b008-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b008-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5b008-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b008-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="5b008-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5b008-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5b008-123">Child elements</span></span>

|<span data-ttu-id="5b008-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b008-124">**Element**</span></span>|<span data-ttu-id="5b008-125">**型**</span><span class="sxs-lookup"><span data-stu-id="5b008-125">**Type**</span></span>|<span data-ttu-id="5b008-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b008-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b008-127">SnapAngle</span><span class="sxs-lookup"><span data-stu-id="5b008-127">SnapAngle</span></span>](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b008-128">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="5b008-128">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b008-129">スナップの角度を度数で指定する浮動小数点数を含みます。</span><span class="sxs-lookup"><span data-stu-id="5b008-129">Contains a floating point number that specifies a snap angle in degrees.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5b008-130">属性</span><span class="sxs-lookup"><span data-stu-id="5b008-130">Attributes</span></span>

<span data-ttu-id="5b008-131">なし。</span><span class="sxs-lookup"><span data-stu-id="5b008-131">None.</span></span>
  

