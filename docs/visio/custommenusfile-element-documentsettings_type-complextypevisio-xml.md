---
title: CustomMenusFile 要素 (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: 文書のカスタムメニューとアクセラレータを定義する Microsoft Visio ユーザーインターフェイス (vsu) ファイルの名前が含まれています。
ms.openlocfilehash: 347660abab266493254b4dc2b47150f3b80fd371
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282902"
---
# <a name="custommenusfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="f225c-103">CustomMenusFile 要素 (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f225c-103">CustomMenusFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f225c-104">文書のカスタムメニューとアクセラレータを定義する Microsoft Visio ユーザーインターフェイス (vsu) ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f225c-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f225c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="f225c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f225c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f225c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f225c-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="f225c-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f225c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f225c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f225c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f225c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f225c-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="f225c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f225c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="f225c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f225c-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="f225c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f225c-113">定義</span><span class="sxs-lookup"><span data-stu-id="f225c-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f225c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f225c-114">Elements and attributes</span></span>

<span data-ttu-id="f225c-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f225c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f225c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f225c-116">Parent elements</span></span>

|<span data-ttu-id="f225c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f225c-117">**Element**</span></span>|<span data-ttu-id="f225c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f225c-118">**Type**</span></span>|<span data-ttu-id="f225c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f225c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f225c-120">documentsettings</span><span class="sxs-lookup"><span data-stu-id="f225c-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f225c-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f225c-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f225c-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="f225c-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f225c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f225c-123">Child elements</span></span>

<span data-ttu-id="f225c-124">なし。</span><span class="sxs-lookup"><span data-stu-id="f225c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f225c-125">属性</span><span class="sxs-lookup"><span data-stu-id="f225c-125">Attributes</span></span>

<span data-ttu-id="f225c-126">なし。</span><span class="sxs-lookup"><span data-stu-id="f225c-126">None.</span></span>
  

