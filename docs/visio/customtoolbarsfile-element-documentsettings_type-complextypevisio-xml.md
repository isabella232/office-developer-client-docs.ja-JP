---
title: CustomToolbarsFile 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: ドキュメントのカスタム ツールバーとステータス バー Visio定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前を含んでいます。
ms.openlocfilehash: c374bc571163936ccdd4812bcf58a8db19a81f1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539235"
---
# <a name="customtoolbarsfile-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="b7f9b-103">CustomToolbarsFile 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b7f9b-103">CustomToolbarsFile element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b7f9b-104">ドキュメントのカスタム ツールバーとステータス バー Visio定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="b7f9b-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7f9b-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="b7f9b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f9b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b7f9b-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="b7f9b-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b7f9b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b7f9b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b7f9b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b7f9b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b7f9b-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b7f9b-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="b7f9b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7f9b-113">定義</span><span class="sxs-lookup"><span data-stu-id="b7f9b-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7f9b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b7f9b-114">Elements and attributes</span></span>

<span data-ttu-id="b7f9b-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7f9b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b7f9b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b7f9b-116">Parent elements</span></span>

|<span data-ttu-id="b7f9b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-117">**Element**</span></span>|<span data-ttu-id="b7f9b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-118">**Type**</span></span>|<span data-ttu-id="b7f9b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b7f9b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7f9b-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="b7f9b-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7f9b-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b7f9b-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7f9b-122">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b7f9b-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7f9b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b7f9b-123">Child elements</span></span>

<span data-ttu-id="b7f9b-124">なし。</span><span class="sxs-lookup"><span data-stu-id="b7f9b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7f9b-125">属性</span><span class="sxs-lookup"><span data-stu-id="b7f9b-125">Attributes</span></span>

<span data-ttu-id="b7f9b-126">なし。</span><span class="sxs-lookup"><span data-stu-id="b7f9b-126">None.</span></span>
  

