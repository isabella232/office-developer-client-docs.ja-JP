---
title: CustomToolbarsFile 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: ユーザー設定ツールバーおよびドキュメントのステータス バーを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。
ms.openlocfilehash: 3744caeb09e1fe865c9e669b9cacfada4cbef1c7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392908"
---
# <a name="customtoolbarsfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="59d6e-103">CustomToolbarsFile 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="59d6e-103">CustomToolbarsFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="59d6e-104">ユーザー設定ツールバーおよびドキュメントのステータス バーを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59d6e-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59d6e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="59d6e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59d6e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="59d6e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="59d6e-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="59d6e-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59d6e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="59d6e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59d6e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="59d6e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="59d6e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="59d6e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59d6e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="59d6e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="59d6e-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="59d6e-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59d6e-113">定義</span><span class="sxs-lookup"><span data-stu-id="59d6e-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59d6e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="59d6e-114">Elements and attributes</span></span>

<span data-ttu-id="59d6e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59d6e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59d6e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="59d6e-116">Parent elements</span></span>

|<span data-ttu-id="59d6e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="59d6e-117">**Element**</span></span>|<span data-ttu-id="59d6e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="59d6e-118">**Type**</span></span>|<span data-ttu-id="59d6e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="59d6e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59d6e-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="59d6e-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59d6e-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="59d6e-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59d6e-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59d6e-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59d6e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="59d6e-123">Child elements</span></span>

<span data-ttu-id="59d6e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="59d6e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59d6e-125">属性</span><span class="sxs-lookup"><span data-stu-id="59d6e-125">Attributes</span></span>

<span data-ttu-id="59d6e-126">なし。</span><span class="sxs-lookup"><span data-stu-id="59d6e-126">None.</span></span>
  

