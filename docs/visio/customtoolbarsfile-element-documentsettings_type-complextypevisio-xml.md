---
title: CustomToolbarsFile 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: ユーザー設定ツールバーおよびドキュメントのステータス バーを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。
ms.openlocfilehash: 46abc567d2135815a82b4efec47a7bd77d0763cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805155"
---
# <a name="customtoolbarsfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="81272-103">CustomToolbarsFile 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="81272-103">CustomToolbarsFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="81272-104">ユーザー設定ツールバーおよびドキュメントのステータス バーを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81272-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81272-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="81272-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81272-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="81272-106">**Element type**</span></span> <br/> |[<span data-ttu-id="81272-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="81272-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="81272-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="81272-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="81272-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="81272-109">**Schema file**</span></span> <br/> |<span data-ttu-id="81272-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="81272-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="81272-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="81272-111">**Document parts**</span></span> <br/> |<span data-ttu-id="81272-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="81272-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81272-113">定義</span><span class="sxs-lookup"><span data-stu-id="81272-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="81272-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="81272-114">Elements and attributes</span></span>

<span data-ttu-id="81272-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="81272-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="81272-116">親要素</span><span class="sxs-lookup"><span data-stu-id="81272-116">Parent elements</span></span>

|<span data-ttu-id="81272-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="81272-117">**Element**</span></span>|<span data-ttu-id="81272-118">**型**</span><span class="sxs-lookup"><span data-stu-id="81272-118">**Type**</span></span>|<span data-ttu-id="81272-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="81272-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81272-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="81272-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="81272-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="81272-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="81272-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81272-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="81272-123">子要素</span><span class="sxs-lookup"><span data-stu-id="81272-123">Child elements</span></span>

<span data-ttu-id="81272-124">なし。</span><span class="sxs-lookup"><span data-stu-id="81272-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81272-125">属性</span><span class="sxs-lookup"><span data-stu-id="81272-125">Attributes</span></span>

<span data-ttu-id="81272-126">なし。</span><span class="sxs-lookup"><span data-stu-id="81272-126">None.</span></span>
  

