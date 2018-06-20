---
title: PropertyDefinition ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803713"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="76507-103">PropertyDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="76507-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="76507-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76507-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76507-105">PropertyDefinition ストリームの構造体は、Microsoft Outlook アイテム内のすべてのユーザー定義フィールドの定義で、いくつかの組み込みのフィールドのデータ バインディングの設定を含む[FieldDefinition](fielddefinition-stream-structure.md)ストリームの構造体の配列です。</span><span class="sxs-lookup"><span data-stu-id="76507-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="76507-106">PropertyDefinition ストリームの構造体をプログラムで操作できます。</span><span class="sxs-lookup"><span data-stu-id="76507-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="76507-107">ただし、Outlook のフォーム デザイナーを使用して同様の結果を達成することができ、データ バインド コントロールの**プロパティ**ダイアログ ボックスが具体的には、します。</span><span class="sxs-lookup"><span data-stu-id="76507-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="76507-108">PropertyDefinition ストリームの構造体のフィールド定義には、2 つの形式のいずれかを指定できます: PropDefV1 と PropDefV2。</span><span class="sxs-lookup"><span data-stu-id="76507-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="76507-109">Outlook には、PropDefV1 と PropDefV2 の両方がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="76507-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="76507-110">PropertyDefinition ストリームの構造体を 1 つですべてのフィールドの定義は、同じ形式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="76507-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="76507-111">PropDefV1 と PropDefV2 の違いの詳細については、 [FieldDefinition ストリームの構造体](fielddefinition-stream-structure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76507-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="76507-112">このストリーム内のデータ要素は、以下に指定した順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。</span><span class="sxs-lookup"><span data-stu-id="76507-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="76507-113">バージョン: ワード (2 バイト) を PropertyDefinition 内のフィールド定義の形式ストリームの構造体です。</span><span class="sxs-lookup"><span data-stu-id="76507-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="76507-114">次の表は、可能な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="76507-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="76507-115">**値**</span><span class="sxs-lookup"><span data-stu-id="76507-115">**Value**</span></span>|<span data-ttu-id="76507-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="76507-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="76507-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="76507-117">0x0102</span></span>  <br/> |<span data-ttu-id="76507-118">形式は、PropDefV1 です。</span><span class="sxs-lookup"><span data-stu-id="76507-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="76507-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="76507-119">0x0103</span></span>  <br/> |<span data-ttu-id="76507-120">形式は、PropDefV2 です。</span><span class="sxs-lookup"><span data-stu-id="76507-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="76507-121">FieldDefinitionCount: DWORD (4 バイト) で、このストリーム内のフィールドの定義の数です。</span><span class="sxs-lookup"><span data-stu-id="76507-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="76507-122">これは、FieldDefinitions のデータ要素の配列の要素の数です。</span><span class="sxs-lookup"><span data-stu-id="76507-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="76507-123">FieldDefinitions: FieldDefinition ストリームの構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="76507-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="76507-124">この配列は、FieldDefinitionCount のデータ要素と同じです。</span><span class="sxs-lookup"><span data-stu-id="76507-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76507-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="76507-125">See also</span></span>

- [<span data-ttu-id="76507-126">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="76507-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="76507-127">新しいユーザー定義フィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="76507-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="76507-128">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="76507-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="76507-129">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="76507-129">Stream Structures</span></span>](stream-structures.md)

