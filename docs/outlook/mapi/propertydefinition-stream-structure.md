---
title: PropertyDefinition ストリーム構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438590"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="ad2b9-103">PropertyDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="ad2b9-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="ad2b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad2b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad2b9-105">PropertyDefinition ストリーム構造は、Microsoft Outlook アイテム内のすべてのユーザー定義フィールドの定義と、一部の組み込みフィールドのデータ バインド設定を含む[FieldDefinition](fielddefinition-stream-structure.md)ストリーム構造の配列です。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="ad2b9-106">PropertyDefinition ストリーム構造をプログラムで操作できます。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ad2b9-107">ただし、データ バインド コントロールの Outlookフォーム デザイナー、特に [プロパティ] ダイアログボックスを使用すると、同様の結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="ad2b9-108">PropertyDefinition ストリーム構造のフィールド定義には、PropDefV1 と PropDefV2 の 2 つの形式のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ad2b9-109">Outlook PropDefV1 と PropDefV2 の両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ad2b9-110">単一の PropertyDefinition ストリーム構造内のすべてのフィールド定義は、同じ形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="ad2b9-111">PropDefV1 と PropDefV2 の違いについて詳しくは [、「FieldDefinition ストリーム構造」をご覧ください](fielddefinition-stream-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="ad2b9-112">このストリーム内のデータ要素は、リトル エンディアン バイト順に格納され、次に示す順序で互いに直後に格納されます。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="ad2b9-113">バージョン: WORD (2 バイト)、PropertyDefinition ストリーム構造内のフィールド定義の形式。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ad2b9-114">以下の表に使用できる値を示します。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="ad2b9-115">**値**</span><span class="sxs-lookup"><span data-stu-id="ad2b9-115">**Value**</span></span>|<span data-ttu-id="ad2b9-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad2b9-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="ad2b9-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="ad2b9-117">0x0102</span></span>  <br/> |<span data-ttu-id="ad2b9-118">形式は PropDefV1 です。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="ad2b9-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="ad2b9-119">0x0103</span></span>  <br/> |<span data-ttu-id="ad2b9-120">形式は PropDefV2 です。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="ad2b9-121">FieldDefinitionCount: DWORD (4 バイト)、このストリーム内のフィールド定義の数。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="ad2b9-122">これは、FieldDefinitions データ要素内の配列要素の数です。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="ad2b9-123">FieldDefinitions: FieldDefinition ストリーム構造の配列。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="ad2b9-124">この配列の数は、FieldDefinitionCount データ要素と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="ad2b9-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad2b9-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad2b9-125">See also</span></span>

- [<span data-ttu-id="ad2b9-126">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="ad2b9-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="ad2b9-127">新しいフィールドの定義をUser-Definedする</span><span class="sxs-lookup"><span data-stu-id="ad2b9-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="ad2b9-128">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="ad2b9-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="ad2b9-129">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="ad2b9-129">Stream Structures</span></span>](stream-structures.md)

