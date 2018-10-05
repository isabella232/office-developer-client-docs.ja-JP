---
title: ProtectMasters 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: 作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。 ユーザーこの設定に関係なく、マスター シェイプから新しい図形を作成できます。
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386447"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="8b41c-104">ProtectMasters 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="8b41c-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8b41c-105">作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8b41c-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="8b41c-106">ユーザーこの設定に関係なく、マスター シェイプから新しい図形を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8b41c-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="8b41c-107">この要素に指定できる値の範囲は、'0' または '1' のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="8b41c-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="8b41c-108">'0' の値は、ユーザーを作成、編集、または削除できるマスター シェイプを示します。</span><span class="sxs-lookup"><span data-stu-id="8b41c-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="8b41c-109">'1' の値は、あるユーザーを作成、編集、または削除できないマスター シェイプを示します。</span><span class="sxs-lookup"><span data-stu-id="8b41c-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b41c-110">要素情報</span><span class="sxs-lookup"><span data-stu-id="8b41c-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b41c-111">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8b41c-111">**Element type**</span></span> <br/> |[<span data-ttu-id="8b41c-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="8b41c-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8b41c-113">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8b41c-113">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8b41c-114">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8b41c-114">**Schema file**</span></span> <br/> |<span data-ttu-id="8b41c-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8b41c-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8b41c-116">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8b41c-116">**Document parts**</span></span> <br/> |<span data-ttu-id="8b41c-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="8b41c-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b41c-118">定義</span><span class="sxs-lookup"><span data-stu-id="8b41c-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8b41c-119">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8b41c-119">Elements and attributes</span></span>

<span data-ttu-id="8b41c-120">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b41c-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8b41c-121">親要素</span><span class="sxs-lookup"><span data-stu-id="8b41c-121">Parent elements</span></span>

|<span data-ttu-id="8b41c-122">**要素**</span><span class="sxs-lookup"><span data-stu-id="8b41c-122">**Element**</span></span>|<span data-ttu-id="8b41c-123">**型**</span><span class="sxs-lookup"><span data-stu-id="8b41c-123">**Type**</span></span>|<span data-ttu-id="8b41c-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b41c-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b41c-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="8b41c-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8b41c-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="8b41c-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8b41c-127">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b41c-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b41c-128">子要素</span><span class="sxs-lookup"><span data-stu-id="8b41c-128">Child elements</span></span>

<span data-ttu-id="8b41c-129">なし。</span><span class="sxs-lookup"><span data-stu-id="8b41c-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b41c-130">属性</span><span class="sxs-lookup"><span data-stu-id="8b41c-130">Attributes</span></span>

<span data-ttu-id="8b41c-131">なし。</span><span class="sxs-lookup"><span data-stu-id="8b41c-131">None.</span></span>
  

