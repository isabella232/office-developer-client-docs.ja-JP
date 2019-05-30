---
title: CustomToolbarsFile 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: 文書のカスタムツールバーおよびステータスバーを定義する Microsoft Visio ユーザーインターフェイス (vsu) ファイルの名前が含まれています。
ms.openlocfilehash: c374bc571163936ccdd4812bcf58a8db19a81f1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539235"
---
# <a name="customtoolbarsfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="f9c56-103">CustomToolbarsFile 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f9c56-103">CustomToolbarsFile element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f9c56-104">文書のカスタムツールバーおよびステータスバーを定義する Microsoft Visio ユーザーインターフェイス (vsu) ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9c56-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9c56-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="f9c56-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9c56-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f9c56-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f9c56-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="f9c56-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f9c56-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f9c56-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f9c56-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f9c56-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f9c56-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="f9c56-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f9c56-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="f9c56-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f9c56-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="f9c56-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9c56-113">定義</span><span class="sxs-lookup"><span data-stu-id="f9c56-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f9c56-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f9c56-114">Elements and attributes</span></span>

<span data-ttu-id="f9c56-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9c56-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f9c56-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f9c56-116">Parent elements</span></span>

|<span data-ttu-id="f9c56-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f9c56-117">**Element**</span></span>|<span data-ttu-id="f9c56-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f9c56-118">**Type**</span></span>|<span data-ttu-id="f9c56-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f9c56-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9c56-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="f9c56-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f9c56-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f9c56-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f9c56-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="f9c56-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f9c56-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f9c56-123">Child elements</span></span>

<span data-ttu-id="f9c56-124">なし。</span><span class="sxs-lookup"><span data-stu-id="f9c56-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9c56-125">属性</span><span class="sxs-lookup"><span data-stu-id="f9c56-125">Attributes</span></span>

<span data-ttu-id="f9c56-126">なし。</span><span class="sxs-lookup"><span data-stu-id="f9c56-126">None.</span></span>
  

