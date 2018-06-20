---
title: ProtectMasters 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: 作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。 ユーザーこの設定に関係なく、マスター シェイプから新しい図形を作成できます。
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806111"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="e998f-104">ProtectMasters 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e998f-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e998f-105">作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e998f-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="e998f-106">ユーザーこの設定に関係なく、マスター シェイプから新しい図形を作成できます。</span><span class="sxs-lookup"><span data-stu-id="e998f-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="e998f-107">この要素に指定できる値の範囲は、'0' または '1' のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="e998f-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="e998f-108">'0' の値は、ユーザーを作成、編集、または削除できるマスター シェイプを示します。</span><span class="sxs-lookup"><span data-stu-id="e998f-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="e998f-109">'1' の値は、あるユーザーを作成、編集、または削除できないマスター シェイプを示します。</span><span class="sxs-lookup"><span data-stu-id="e998f-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e998f-110">要素情報</span><span class="sxs-lookup"><span data-stu-id="e998f-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e998f-111">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="e998f-111">**Element type**</span></span> <br/> |[<span data-ttu-id="e998f-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="e998f-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e998f-113">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e998f-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e998f-114">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e998f-114">**Schema file**</span></span> <br/> |<span data-ttu-id="e998f-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e998f-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e998f-116">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e998f-116">**Document parts**</span></span> <br/> |<span data-ttu-id="e998f-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="e998f-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e998f-118">定義</span><span class="sxs-lookup"><span data-stu-id="e998f-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e998f-119">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e998f-119">Elements and attributes</span></span>

<span data-ttu-id="e998f-120">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e998f-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e998f-121">親要素</span><span class="sxs-lookup"><span data-stu-id="e998f-121">Parent elements</span></span>

|<span data-ttu-id="e998f-122">**要素**</span><span class="sxs-lookup"><span data-stu-id="e998f-122">**Element**</span></span>|<span data-ttu-id="e998f-123">**型**</span><span class="sxs-lookup"><span data-stu-id="e998f-123">**Type**</span></span>|<span data-ttu-id="e998f-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="e998f-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e998f-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="e998f-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e998f-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e998f-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e998f-127">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e998f-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e998f-128">子要素</span><span class="sxs-lookup"><span data-stu-id="e998f-128">Child elements</span></span>

<span data-ttu-id="e998f-129">なし。</span><span class="sxs-lookup"><span data-stu-id="e998f-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e998f-130">属性</span><span class="sxs-lookup"><span data-stu-id="e998f-130">Attributes</span></span>

<span data-ttu-id="e998f-131">なし。</span><span class="sxs-lookup"><span data-stu-id="e998f-131">None.</span></span>
  

