---
title: ProtectMasters 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: ユーザーがマスター 図形の作成、編集、または削除を防止するかどうかを指定します。 ユーザーは、この設定に関係なく、マスター図形から新しい図形を作成できます。
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540694"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="51d71-104">ProtectMasters 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="51d71-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="51d71-105">ユーザーがマスター 図形の作成、編集、または削除を防止するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="51d71-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="51d71-106">ユーザーは、この設定に関係なく、マスター図形から新しい図形を作成できます。</span><span class="sxs-lookup"><span data-stu-id="51d71-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="51d71-107">この要素で使用できる値の範囲は、'0' または '1' です。</span><span class="sxs-lookup"><span data-stu-id="51d71-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="51d71-108">値 '0' は、ユーザーがマスター シェイプを作成、編集、または削除できる状態を示します。</span><span class="sxs-lookup"><span data-stu-id="51d71-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="51d71-109">値 '1' は、ユーザーがマスター 図形を作成、編集、または削除できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="51d71-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51d71-110">要素の情報</span><span class="sxs-lookup"><span data-stu-id="51d71-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51d71-111">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="51d71-111">**Element type**</span></span> <br/> |[<span data-ttu-id="51d71-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="51d71-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="51d71-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="51d71-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="51d71-114">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="51d71-114">**Schema file**</span></span> <br/> |<span data-ttu-id="51d71-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="51d71-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="51d71-116">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="51d71-116">**Document parts**</span></span> <br/> |<span data-ttu-id="51d71-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="51d71-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="51d71-118">定義</span><span class="sxs-lookup"><span data-stu-id="51d71-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="51d71-119">要素と属性</span><span class="sxs-lookup"><span data-stu-id="51d71-119">Elements and attributes</span></span>

<span data-ttu-id="51d71-120">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="51d71-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="51d71-121">親要素</span><span class="sxs-lookup"><span data-stu-id="51d71-121">Parent elements</span></span>

|<span data-ttu-id="51d71-122">**要素**</span><span class="sxs-lookup"><span data-stu-id="51d71-122">**Element**</span></span>|<span data-ttu-id="51d71-123">**型**</span><span class="sxs-lookup"><span data-stu-id="51d71-123">**Type**</span></span>|<span data-ttu-id="51d71-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="51d71-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="51d71-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="51d71-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="51d71-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="51d71-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="51d71-127">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="51d71-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="51d71-128">子要素</span><span class="sxs-lookup"><span data-stu-id="51d71-128">Child elements</span></span>

<span data-ttu-id="51d71-129">なし。</span><span class="sxs-lookup"><span data-stu-id="51d71-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51d71-130">属性</span><span class="sxs-lookup"><span data-stu-id="51d71-130">Attributes</span></span>

<span data-ttu-id="51d71-131">なし。</span><span class="sxs-lookup"><span data-stu-id="51d71-131">None.</span></span>
  

