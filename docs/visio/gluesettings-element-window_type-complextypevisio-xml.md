---
title: GlueSettings 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b5292f82-f299-ea96-6101-ebb799bbec9a
description: ドキュメントで接着が有効になっているときに図形が接着するオブジェクトを指定します。
ms.openlocfilehash: 53cec76448d0779b3068822388d5b874f4754eb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805477"
---
# <a name="gluesettings-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="99b4f-103">GlueSettings 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="99b4f-103">GlueSettings element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="99b4f-104">ドキュメントで接着が有効になっているときに図形が接着するオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="99b4f-104">Specifies the objects that shapes glue to when glue is enabled in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99b4f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="99b4f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99b4f-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="99b4f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="99b4f-107">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="99b4f-107">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="99b4f-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="99b4f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="99b4f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="99b4f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="99b4f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="99b4f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="99b4f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="99b4f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="99b4f-112">windows.xml、document.xml</span><span class="sxs-lookup"><span data-stu-id="99b4f-112">windows.xml, document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99b4f-113">定義</span><span class="sxs-lookup"><span data-stu-id="99b4f-113">Definition</span></span>

```XML
< xs:element name="GlueSettings" type="GlueSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="99b4f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="99b4f-114">Elements and attributes</span></span>

<span data-ttu-id="99b4f-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="99b4f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="99b4f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="99b4f-116">Parent elements</span></span>

|<span data-ttu-id="99b4f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="99b4f-117">**Element**</span></span>|<span data-ttu-id="99b4f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="99b4f-118">**Type**</span></span>|<span data-ttu-id="99b4f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="99b4f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99b4f-120">Window</span><span class="sxs-lookup"><span data-stu-id="99b4f-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="99b4f-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="99b4f-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="99b4f-122">Microsoft Visio のインスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="99b4f-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99b4f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="99b4f-123">Child elements</span></span>

<span data-ttu-id="99b4f-124">なし。</span><span class="sxs-lookup"><span data-stu-id="99b4f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99b4f-125">属性</span><span class="sxs-lookup"><span data-stu-id="99b4f-125">Attributes</span></span>

<span data-ttu-id="99b4f-126">なし。</span><span class="sxs-lookup"><span data-stu-id="99b4f-126">None.</span></span>
  

