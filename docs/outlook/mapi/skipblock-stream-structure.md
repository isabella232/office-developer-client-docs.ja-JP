---
title: SkipBlock ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b7be498473ef86b11006702f85089f0f95bb2e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580902"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="1d5db-103">SkipBlock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="1d5db-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="1d5db-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d5db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d5db-105">SkipBlock ストリームの構造体は、ブロックの残りの部分の長さを指定する整数値で始まるデータのブロックです。</span><span class="sxs-lookup"><span data-stu-id="1d5db-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="1d5db-106">このストリームの構造体は、フィールド定義は、PropDefV2 形式の場合、 [FieldDefinition](fielddefinition-stream-structure.md)ストリームに存在します。</span><span class="sxs-lookup"><span data-stu-id="1d5db-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="1d5db-107">SkipBlock ストリームの構造体の目的は、FieldDefinition ストリームの SkipBlocks のデータ要素の構造体のような一連の相対位置によって異なります。</span><span class="sxs-lookup"><span data-stu-id="1d5db-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="1d5db-108">SkipBlocks シリーズは、シリーズを終了し、0 に等しいサイズのデータ要素を持つことが少なくとも 1 つの SkipBlock 構造体を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5db-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="1d5db-109">最初の構造は、終端の構造ではない場合 (つまり、サイズのデータ要素が 0 より大きい)、Outlook は、最初の構造体は、Unicode (utf-16) でフィールド名を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d5db-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="1d5db-110">このストリーム内のデータ要素は、以下に指定した順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。</span><span class="sxs-lookup"><span data-stu-id="1d5db-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="1d5db-111">サイズ: DWORD (4 バイト) で、サイズ、コンテンツのデータ要素のバイト単位の数。</span><span class="sxs-lookup"><span data-stu-id="1d5db-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="1d5db-112">コンテンツ: バイトの配列。</span><span class="sxs-lookup"><span data-stu-id="1d5db-112">Content: An array of BYTE.</span></span> <span data-ttu-id="1d5db-113">この配列は、サイズのデータ要素と同じです。</span><span class="sxs-lookup"><span data-stu-id="1d5db-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="1d5db-114">コンテンツのデータ要素の意味は、一連の SkipBlock 構造体の場所や Outlook のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1d5db-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="1d5db-115">最初の SkipBlock 構造体が終端構造でない場合は、Outlook では Unicode でフィールド名を指定する[FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)ストリームの構造体として最初の SkipBlock 構造体が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="1d5db-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1d5db-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d5db-116">See also</span></span>



[<span data-ttu-id="1d5db-117">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="1d5db-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="1d5db-118">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="1d5db-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="1d5db-119">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="1d5db-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="1d5db-120">FirstSkipBlockContent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="1d5db-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

