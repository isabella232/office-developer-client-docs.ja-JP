---
title: cp 要素 (Text_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: 文字プロパティの最初の実行されているマークは、対応する Char 要素に従って書式設定されました。 実行は、次のタグまで、テキストの末尾に定義されています。
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388197"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="94bdf-104">cp 要素 (Text_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="94bdf-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="94bdf-105">文字プロパティの最初の実行されているマークは、対応する Char 要素に従って書式設定されました。</span><span class="sxs-lookup"><span data-stu-id="94bdf-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="94bdf-106">実行は、次のタグまで、テキストの末尾に定義されています。</span><span class="sxs-lookup"><span data-stu-id="94bdf-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94bdf-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="94bdf-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94bdf-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="94bdf-108">**Element type**</span></span> <br/> |[<span data-ttu-id="94bdf-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="94bdf-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="94bdf-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="94bdf-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="94bdf-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="94bdf-111">**Schema file**</span></span> <br/> |<span data-ttu-id="94bdf-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="94bdf-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="94bdf-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="94bdf-113">**Document parts**</span></span> <br/> |<span data-ttu-id="94bdf-114"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="94bdf-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94bdf-115">定義</span><span class="sxs-lookup"><span data-stu-id="94bdf-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="94bdf-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="94bdf-116">Elements and attributes</span></span>

<span data-ttu-id="94bdf-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="94bdf-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="94bdf-118">親要素</span><span class="sxs-lookup"><span data-stu-id="94bdf-118">Parent elements</span></span>

|<span data-ttu-id="94bdf-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="94bdf-119">**Element**</span></span>|<span data-ttu-id="94bdf-120">**型**</span><span class="sxs-lookup"><span data-stu-id="94bdf-120">**Type**</span></span>|<span data-ttu-id="94bdf-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="94bdf-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="94bdf-122">Text</span><span class="sxs-lookup"><span data-stu-id="94bdf-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="94bdf-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="94bdf-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94bdf-124">図形のテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="94bdf-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94bdf-125">子要素</span><span class="sxs-lookup"><span data-stu-id="94bdf-125">Child elements</span></span>

<span data-ttu-id="94bdf-126">なし。</span><span class="sxs-lookup"><span data-stu-id="94bdf-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94bdf-127">属性</span><span class="sxs-lookup"><span data-stu-id="94bdf-127">Attributes</span></span>

|<span data-ttu-id="94bdf-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="94bdf-128">**Attribute**</span></span>|<span data-ttu-id="94bdf-129">**型**</span><span class="sxs-lookup"><span data-stu-id="94bdf-129">**Type**</span></span>|<span data-ttu-id="94bdf-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="94bdf-130">**Required**</span></span>|<span data-ttu-id="94bdf-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="94bdf-131">**Description**</span></span>|<span data-ttu-id="94bdf-132">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="94bdf-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94bdf-133">IX</span><span class="sxs-lookup"><span data-stu-id="94bdf-133">IX</span></span>  <br/> |<span data-ttu-id="94bdf-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="94bdf-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="94bdf-135">必須</span><span class="sxs-lookup"><span data-stu-id="94bdf-135">required</span></span>  <br/> |<span data-ttu-id="94bdf-136">このプロパティの実行を表す Char 要素のインデックス。</span><span class="sxs-lookup"><span data-stu-id="94bdf-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="94bdf-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="94bdf-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

