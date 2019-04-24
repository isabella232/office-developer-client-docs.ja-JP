---
title: ProtectMasters 要素 (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: ユーザーがマスターシェイプの作成、編集、または削除をできないようにするかどうかを指定します。 ユーザーは、この設定に関係なく、マスターシェイプから新しい図形を作成することができます。
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314820"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="0e1cd-104">ProtectMasters 要素 (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0e1cd-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0e1cd-105">ユーザーがマスターシェイプの作成、編集、または削除をできないようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="0e1cd-106">ユーザーは、この設定に関係なく、マスターシェイプから新しい図形を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="0e1cd-107">この要素で使用できる値の範囲は、' 0 ' または ' 1 ' のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="0e1cd-108">値 ' 0 ' は、ユーザーがマスターシェイプを作成、編集、または削除できることを示します。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="0e1cd-109">値 ' 1 ' は、ユーザーがマスターシェイプを作成、編集、または削除できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e1cd-110">要素情報</span><span class="sxs-lookup"><span data-stu-id="0e1cd-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e1cd-111">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-111">**Element type**</span></span> <br/> |[<span data-ttu-id="0e1cd-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="0e1cd-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0e1cd-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-113">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0e1cd-114">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-114">**Schema file**</span></span> <br/> |<span data-ttu-id="0e1cd-115">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="0e1cd-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0e1cd-116">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-116">**Document parts**</span></span> <br/> |<span data-ttu-id="0e1cd-117">文書の xml</span><span class="sxs-lookup"><span data-stu-id="0e1cd-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e1cd-118">定義</span><span class="sxs-lookup"><span data-stu-id="0e1cd-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0e1cd-119">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0e1cd-119">Elements and attributes</span></span>

<span data-ttu-id="0e1cd-120">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0e1cd-121">親要素</span><span class="sxs-lookup"><span data-stu-id="0e1cd-121">Parent elements</span></span>

|<span data-ttu-id="0e1cd-122">**要素**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-122">**Element**</span></span>|<span data-ttu-id="0e1cd-123">**型**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-123">**Type**</span></span>|<span data-ttu-id="0e1cd-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e1cd-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e1cd-125">documentsettings</span><span class="sxs-lookup"><span data-stu-id="0e1cd-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e1cd-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="0e1cd-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0e1cd-127">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0e1cd-128">子要素</span><span class="sxs-lookup"><span data-stu-id="0e1cd-128">Child elements</span></span>

<span data-ttu-id="0e1cd-129">なし。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e1cd-130">属性</span><span class="sxs-lookup"><span data-stu-id="0e1cd-130">Attributes</span></span>

<span data-ttu-id="0e1cd-131">なし。</span><span class="sxs-lookup"><span data-stu-id="0e1cd-131">None.</span></span>
  

