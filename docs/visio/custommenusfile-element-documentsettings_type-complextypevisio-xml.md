---
title: CustomMenusFile 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: カスタム メニューおよびアクセラレータのドキュメントを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。
ms.openlocfilehash: 2044c7e300dc51df8b8cd03ef861391d04494e0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805133"
---
# <a name="custommenusfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="2b408-103">CustomMenusFile 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="2b408-103">CustomMenusFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2b408-104">カスタム メニューおよびアクセラレータのドキュメントを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b408-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b408-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="2b408-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b408-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="2b408-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2b408-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="2b408-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2b408-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="2b408-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2b408-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2b408-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2b408-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2b408-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2b408-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="2b408-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2b408-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="2b408-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b408-113">定義</span><span class="sxs-lookup"><span data-stu-id="2b408-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2b408-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2b408-114">Elements and attributes</span></span>

<span data-ttu-id="2b408-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b408-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2b408-116">親要素</span><span class="sxs-lookup"><span data-stu-id="2b408-116">Parent elements</span></span>

|<span data-ttu-id="2b408-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="2b408-117">**Element**</span></span>|<span data-ttu-id="2b408-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2b408-118">**Type**</span></span>|<span data-ttu-id="2b408-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="2b408-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b408-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="2b408-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b408-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="2b408-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2b408-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b408-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2b408-123">子要素</span><span class="sxs-lookup"><span data-stu-id="2b408-123">Child elements</span></span>

<span data-ttu-id="2b408-124">なし。</span><span class="sxs-lookup"><span data-stu-id="2b408-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b408-125">属性</span><span class="sxs-lookup"><span data-stu-id="2b408-125">Attributes</span></span>

<span data-ttu-id="2b408-126">なし。</span><span class="sxs-lookup"><span data-stu-id="2b408-126">None.</span></span>
  

