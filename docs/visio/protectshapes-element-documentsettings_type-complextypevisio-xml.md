---
title: ProtectShapes 要素 (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e3835fc6-0ae6-b8c3-b1d0-bf893d4a9470
description: ユーザーが lockselect 要素が1に設定されている図形を選択できないようにするかどうかを指定します。
ms.openlocfilehash: 9f7910123c00a8fd4f5ce47ef099c8c6581f8c07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346803"
---
# <a name="protectshapes-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="d19bd-103">ProtectShapes 要素 (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d19bd-103">ProtectShapes element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d19bd-104">ユーザーが**lockselect**要素が1に設定されている図形を選択できないようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d19bd-104">Specifies whether the user is prevented from selecting shapes that have their **LockSelect** element set to 1.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d19bd-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d19bd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d19bd-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d19bd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d19bd-107">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="d19bd-107">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d19bd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d19bd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d19bd-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d19bd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d19bd-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d19bd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d19bd-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d19bd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d19bd-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="d19bd-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d19bd-113">定義</span><span class="sxs-lookup"><span data-stu-id="d19bd-113">Definition</span></span>

```XML
< xs:element name="ProtectShapes" type="ProtectShapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d19bd-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d19bd-114">Elements and attributes</span></span>

<span data-ttu-id="d19bd-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d19bd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d19bd-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d19bd-116">Parent elements</span></span>

|<span data-ttu-id="d19bd-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d19bd-117">**Element**</span></span>|<span data-ttu-id="d19bd-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d19bd-118">**Type**</span></span>|<span data-ttu-id="d19bd-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d19bd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d19bd-120">documentsettings</span><span class="sxs-lookup"><span data-stu-id="d19bd-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d19bd-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="d19bd-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d19bd-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="d19bd-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d19bd-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d19bd-123">Child elements</span></span>

<span data-ttu-id="d19bd-124">なし。</span><span class="sxs-lookup"><span data-stu-id="d19bd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d19bd-125">属性</span><span class="sxs-lookup"><span data-stu-id="d19bd-125">Attributes</span></span>

<span data-ttu-id="d19bd-126">なし。</span><span class="sxs-lookup"><span data-stu-id="d19bd-126">None.</span></span>
  

