---
title: skipblock ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282671"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="26ea0-103">skipblock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="26ea0-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="26ea0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26ea0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26ea0-105">skipblock ストリーム構造は、ブロックの残りの部分の長さを指定する整数で始まるデータのブロックです。</span><span class="sxs-lookup"><span data-stu-id="26ea0-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="26ea0-106">このストリーム構造は、フィールド定義が PropDefV2 形式である場合に、 [fielddefinition](fielddefinition-stream-structure.md)ストリーム内に存在します。</span><span class="sxs-lookup"><span data-stu-id="26ea0-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="26ea0-107">skipblock ストリーム構造の目的は、fielddefinition stream の skipblock data 要素内の一連の like 構造での相対的な位置に依存します。</span><span class="sxs-lookup"><span data-stu-id="26ea0-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="26ea0-108">skipblocks シリーズには、データ系列を終了し、Size data 要素が0である skipblocks 構造が少なくとも1つ含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26ea0-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="26ea0-109">最初の構造が終端構造ではない場合 (つまり、Size data 要素が0より大きい場合)、Outlook は最初の構造体が Unicode (utf-16) でフィールド名を指定しているものとします。</span><span class="sxs-lookup"><span data-stu-id="26ea0-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="26ea0-110">このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="26ea0-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="26ea0-111">size: data data 要素のバイト単位での DWORD (4 バイト) です。</span><span class="sxs-lookup"><span data-stu-id="26ea0-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="26ea0-112">コンテンツ: バイトの配列。</span><span class="sxs-lookup"><span data-stu-id="26ea0-112">Content: An array of BYTE.</span></span> <span data-ttu-id="26ea0-113">この配列の数は、Size data 要素と同じです。</span><span class="sxs-lookup"><span data-stu-id="26ea0-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="26ea0-114">Content data 要素の意味は、Outlook のデータ系列とバージョンの skipblock 構造体の場所によって異なります。</span><span class="sxs-lookup"><span data-stu-id="26ea0-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="26ea0-115">最初の skipblock 構造が終了構造ではない場合、Outlook は最初の skipblock 構造を、Unicode でフィールド名を指定する[firstskipblockcontent](firstskipblockcontent-stream-structure.md)ストリーム構造体と見なします。</span><span class="sxs-lookup"><span data-stu-id="26ea0-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="26ea0-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="26ea0-116">See also</span></span>



[<span data-ttu-id="26ea0-117">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="26ea0-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="26ea0-118">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="26ea0-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="26ea0-119">fielddefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="26ea0-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="26ea0-120">firstskipblockcontent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="26ea0-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

