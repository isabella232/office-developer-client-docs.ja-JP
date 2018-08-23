---
title: ProtectShapes 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e3835fc6-0ae6-b8c3-b1d0-bf893d4a9470
description: ユーザーがその lockselect] を有効要素を 1 に設定されている図形を選択できないとしているかどうかを指定します。
ms.openlocfilehash: 98bb9c565f0dccc2add4a03e3dd6cd82a52015c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806124"
---
# <a name="protectshapes-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="7c796-103">ProtectShapes 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="7c796-103">ProtectShapes element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7c796-104">ユーザーがその**lockselect] を有効**要素を 1 に設定されている図形を選択できないとしているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7c796-104">Specifies whether the user is prevented from selecting shapes that have their **LockSelect** element set to 1.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7c796-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="7c796-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c796-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="7c796-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7c796-107">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="7c796-107">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7c796-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="7c796-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7c796-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7c796-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7c796-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7c796-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7c796-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="7c796-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7c796-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="7c796-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c796-113">定義</span><span class="sxs-lookup"><span data-stu-id="7c796-113">Definition</span></span>

```XML
< xs:element name="ProtectShapes" type="ProtectShapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c796-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7c796-114">Elements and attributes</span></span>

<span data-ttu-id="7c796-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c796-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7c796-116">親要素</span><span class="sxs-lookup"><span data-stu-id="7c796-116">Parent elements</span></span>

|<span data-ttu-id="7c796-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="7c796-117">**Element**</span></span>|<span data-ttu-id="7c796-118">**型**</span><span class="sxs-lookup"><span data-stu-id="7c796-118">**Type**</span></span>|<span data-ttu-id="7c796-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="7c796-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c796-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="7c796-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c796-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7c796-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c796-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c796-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7c796-123">子要素</span><span class="sxs-lookup"><span data-stu-id="7c796-123">Child elements</span></span>

<span data-ttu-id="7c796-124">なし。</span><span class="sxs-lookup"><span data-stu-id="7c796-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c796-125">属性</span><span class="sxs-lookup"><span data-stu-id="7c796-125">Attributes</span></span>

<span data-ttu-id="7c796-126">なし。</span><span class="sxs-lookup"><span data-stu-id="7c796-126">None.</span></span>
  

