---
title: SkipBlock ストリーム構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435545"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="dc581-103">SkipBlock ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="dc581-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="dc581-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc581-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc581-105">SkipBlock ストリーム構造は、ブロックの残りの部分の長さを指定する整数で始まるデータブロックです。</span><span class="sxs-lookup"><span data-stu-id="dc581-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="dc581-106">フィールド定義が [PropDefV2](fielddefinition-stream-structure.md) 形式の場合、このストリーム構造は FieldDefinition ストリームに存在します。</span><span class="sxs-lookup"><span data-stu-id="dc581-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="dc581-107">SkipBlock ストリーム構造の目的は、FieldDefinition ストリームの SkipBlocks データ要素内の一連の同様の構造の相対位置によって異なります。</span><span class="sxs-lookup"><span data-stu-id="dc581-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="dc581-108">SkipBlocks シリーズには、系列を終了し、Size データ要素が 0 に等しい SkipBlock 構造体を少なくとも 1 つ含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc581-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="dc581-109">最初の構造体が終了構造ではない場合 (つまり、Size データ要素が 0 より大きい場合)、Outlook は Unicode (UTF-16) でフィールド名を指定すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="dc581-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="dc581-110">このストリーム内のデータ要素は、リトル エンディアン バイト順に格納され、次に示す順序で互いに直後に格納されます。</span><span class="sxs-lookup"><span data-stu-id="dc581-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="dc581-111">Size: Content データ要素の DWORD (4 バイト)、サイズ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="dc581-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="dc581-112">コンテンツ: BYTE の配列。</span><span class="sxs-lookup"><span data-stu-id="dc581-112">Content: An array of BYTE.</span></span> <span data-ttu-id="dc581-113">この配列の数は Size データ要素と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="dc581-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="dc581-114">Content データ要素の意味は、系列内の SkipBlock 構造の場所と、データ系列のバージョンによってOutlook。</span><span class="sxs-lookup"><span data-stu-id="dc581-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="dc581-115">最初の SkipBlock 構造体が終了構造ではない場合、Outlook は最初の SkipBlock 構造体を Unicode のフィールド名を指定する[FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)ストリーム構造と見なします。</span><span class="sxs-lookup"><span data-stu-id="dc581-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dc581-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc581-116">See also</span></span>



[<span data-ttu-id="dc581-117">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="dc581-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="dc581-118">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="dc581-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="dc581-119">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="dc581-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="dc581-120">FirstSkipBlockContent ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="dc581-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

