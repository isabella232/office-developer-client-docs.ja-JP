---
title: firstskipblockcontent ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 89814eec-67c1-40b6-91d9-a58c3da0f15e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4804f2c6633095ea9eb38bec990cb1554240f6e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337066"
---
# <a name="firstskipblockcontent-stream-structure"></a><span data-ttu-id="6563b-103">firstskipblockcontent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6563b-103">FirstSkipBlockContent Stream Structure</span></span>

  
  
<span data-ttu-id="6563b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6563b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6563b-105">firstskipblockcontent ストリーム構造は、 [fielddefinition](fielddefinition-stream-structure.md)ストリームの skipblocks データ要素の最初の[skipblock](skipblock-stream-structure.md)構造体の内容です。</span><span class="sxs-lookup"><span data-stu-id="6563b-105">The FirstSkipBlockContent stream structure is the content of the first [SkipBlock](skipblock-stream-structure.md) structure in the SkipBlocks data element of a [FieldDefinition](fielddefinition-stream-structure.md) stream.</span></span> <span data-ttu-id="6563b-106">firstskipblockcontent ストリームは単なる data 要素である FieldName、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="6563b-106">The FirstSkipBlockContent stream is simply a single data element, FieldName:</span></span> 
  
- <span data-ttu-id="6563b-107">FieldName: [PackedUnicodeString](packedunicodestring-stream-structure.md)。フィールド名を指定します。</span><span class="sxs-lookup"><span data-stu-id="6563b-107">FieldName: [PackedUnicodeString](packedunicodestring-stream-structure.md), the field name.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6563b-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="6563b-108">See also</span></span>



[<span data-ttu-id="6563b-109">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="6563b-109">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="6563b-110">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="6563b-110">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="6563b-111">skipblock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6563b-111">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="6563b-112">PackedUnicodeString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="6563b-112">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

