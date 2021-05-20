---
title: CustomMenusFile 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: ドキュメントのカスタム メニューとアクセラレータVisio定義する Microsoft ユーザー インターフェイス (.vsu) ファイルの名前が含まれる。
ms.openlocfilehash: 69eca703acf30a10296c13452c2f3e2a11521cd4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540526"
---
# <a name="custommenusfile-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="c7155-103">CustomMenusFile 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c7155-103">CustomMenusFile element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c7155-104">ドキュメントのカスタム メニューとアクセラレータVisio定義する Microsoft ユーザー インターフェイス (.vsu) ファイルの名前が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c7155-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7155-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="c7155-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7155-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c7155-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c7155-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="c7155-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c7155-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c7155-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c7155-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c7155-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c7155-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c7155-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c7155-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="c7155-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c7155-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="c7155-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c7155-113">定義</span><span class="sxs-lookup"><span data-stu-id="c7155-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c7155-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c7155-114">Elements and attributes</span></span>

<span data-ttu-id="c7155-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7155-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c7155-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c7155-116">Parent elements</span></span>

|<span data-ttu-id="c7155-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c7155-117">**Element**</span></span>|<span data-ttu-id="c7155-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c7155-118">**Type**</span></span>|<span data-ttu-id="c7155-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c7155-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c7155-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="c7155-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c7155-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c7155-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c7155-122">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c7155-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c7155-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c7155-123">Child elements</span></span>

<span data-ttu-id="c7155-124">なし。</span><span class="sxs-lookup"><span data-stu-id="c7155-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7155-125">属性</span><span class="sxs-lookup"><span data-stu-id="c7155-125">Attributes</span></span>

<span data-ttu-id="c7155-126">なし。</span><span class="sxs-lookup"><span data-stu-id="c7155-126">None.</span></span>
  

