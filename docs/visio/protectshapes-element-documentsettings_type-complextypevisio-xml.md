---
title: ProtectShapes 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e3835fc6-0ae6-b8c3-b1d0-bf893d4a9470
description: ユーザーが LockSelect 要素が 1 に設定されている図形を選択しないかどうかを指定します。
ms.openlocfilehash: f022c5a0be37f18c0cf0c10dbf18e6a90065e911
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540666"
---
# <a name="protectshapes-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="ea5ea-103">ProtectShapes 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ea5ea-103">ProtectShapes element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ea5ea-104">ユーザーが **LockSelect** 要素が 1 に設定されている図形を選択しないかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ea5ea-104">Specifies whether the user is prevented from selecting shapes that have their **LockSelect** element set to 1.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ea5ea-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ea5ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea5ea-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ea5ea-107">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="ea5ea-107">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ea5ea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ea5ea-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ea5ea-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ea5ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ea5ea-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ea5ea-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="ea5ea-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ea5ea-113">定義</span><span class="sxs-lookup"><span data-stu-id="ea5ea-113">Definition</span></span>

```XML
< xs:element name="ProtectShapes" type="ProtectShapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ea5ea-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ea5ea-114">Elements and attributes</span></span>

<span data-ttu-id="ea5ea-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea5ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ea5ea-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ea5ea-116">Parent elements</span></span>

|<span data-ttu-id="ea5ea-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-117">**Element**</span></span>|<span data-ttu-id="ea5ea-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-118">**Type**</span></span>|<span data-ttu-id="ea5ea-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea5ea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea5ea-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="ea5ea-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ea5ea-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ea5ea-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ea5ea-122">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ea5ea-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ea5ea-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ea5ea-123">Child elements</span></span>

<span data-ttu-id="ea5ea-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ea5ea-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea5ea-125">属性</span><span class="sxs-lookup"><span data-stu-id="ea5ea-125">Attributes</span></span>

<span data-ttu-id="ea5ea-126">なし。</span><span class="sxs-lookup"><span data-stu-id="ea5ea-126">None.</span></span>
  

