---
title: propertydefinition ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328484"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="a16b3-103">propertydefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="a16b3-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="a16b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a16b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a16b3-105">propertydefinition ストリーム構造は、Microsoft Outlook アイテムのすべてのユーザー定義フィールドの定義と、いくつかの組み込みフィールドのデータバインド設定を含む[fielddefinition](fielddefinition-stream-structure.md) stream 構造の配列です。</span><span class="sxs-lookup"><span data-stu-id="a16b3-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="a16b3-106">プログラムを使用して、propertydefinition ストリームの構造を操作できます。</span><span class="sxs-lookup"><span data-stu-id="a16b3-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="a16b3-107">ただし、Outlook フォームデザイナーおよび特に、データ連結コントロールの [**プロパティ**] ダイアログボックスを使用して、同様の結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="a16b3-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="a16b3-108">propertydefinition stream 構造のフィールド定義は、PropDefV1 と PropDefV2 の2つの形式のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a16b3-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="a16b3-109">Outlook では、PropDefV1 と PropDefV2 の両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a16b3-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="a16b3-110">単一の propertydefinition stream 構造のすべてのフィールド定義は、同じ形式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a16b3-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="a16b3-111">PropDefV1 と PropDefV2 の相違点の詳細については、「 [fielddefinition Stream Structure](fielddefinition-stream-structure.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a16b3-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="a16b3-112">このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="a16b3-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="a16b3-113">バージョン: WORD (2 バイト)。 propertydefinition stream 構造のフィールド定義の形式です。</span><span class="sxs-lookup"><span data-stu-id="a16b3-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="a16b3-114">以下の表に使用できる値を示します。</span><span class="sxs-lookup"><span data-stu-id="a16b3-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="a16b3-115">**値**</span><span class="sxs-lookup"><span data-stu-id="a16b3-115">**Value**</span></span>|<span data-ttu-id="a16b3-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="a16b3-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="a16b3-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="a16b3-117">0x0102</span></span>  <br/> |<span data-ttu-id="a16b3-118">形式は PropDefV1 です。</span><span class="sxs-lookup"><span data-stu-id="a16b3-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="a16b3-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="a16b3-119">0x0103</span></span>  <br/> |<span data-ttu-id="a16b3-120">形式は PropDefV2 です。</span><span class="sxs-lookup"><span data-stu-id="a16b3-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="a16b3-121">fielddefinitioncount: このストリーム内のフィールド定義の数である DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="a16b3-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="a16b3-122">fielddefinitions data 要素の配列要素の数を示します。</span><span class="sxs-lookup"><span data-stu-id="a16b3-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="a16b3-123">fielddefinitions: fielddefinitions ストリーム構造の配列。</span><span class="sxs-lookup"><span data-stu-id="a16b3-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="a16b3-124">この配列の数は、fielddefinitioncount data 要素と同じです。</span><span class="sxs-lookup"><span data-stu-id="a16b3-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a16b3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a16b3-125">See also</span></span>

- [<span data-ttu-id="a16b3-126">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="a16b3-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="a16b3-127">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="a16b3-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="a16b3-128">propertydefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="a16b3-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="a16b3-129">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="a16b3-129">Stream Structures</span></span>](stream-structures.md)

