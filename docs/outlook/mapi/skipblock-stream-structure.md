---
title: SkipBlock ストリーム構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fd4dfba1aaa13294fc1a238e9d4cfac28831849e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624210"
---
# <a name="skipblock-stream-structure"></a>SkipBlock ストリーム構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
SkipBlock ストリーム構造は、ブロックの残りの部分の長さを指定する整数で始まるデータブロックです。 フィールド定義が [PropDefV2](fielddefinition-stream-structure.md) 形式の場合、このストリーム構造は FieldDefinition ストリームに存在します。 
  
SkipBlock ストリーム構造の目的は、FieldDefinition ストリームの SkipBlocks データ要素内の一連の同様の構造の相対位置によって異なります。 SkipBlocks シリーズには、系列を終了し、Size データ要素が 0 に等しい SkipBlock 構造体を少なくとも 1 つ含む必要があります。 最初の構造体が終了構造ではない場合 (つまり、Size データ要素が 0 より大きい場合)、Outlook は Unicode (UTF-16) でフィールド名を指定すると仮定します。
  
このストリーム内のデータ要素は、リトル エンディアン バイト順に格納され、次に示す順序で互いに直後に格納されます。
  
- Size: Content データ要素の DWORD (4 バイト)、サイズ (バイト数)。
    
- コンテンツ: BYTE の配列。 この配列の数は Size データ要素と等しくなります。 Content データ要素の意味は、系列内の SkipBlock 構造の場所と、データ系列のバージョンによってOutlook。 最初の SkipBlock 構造体が終了構造ではない場合、Outlook は最初の SkipBlock 構造体を Unicode のフィールド名を指定する[FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)ストリーム構造と見なします。 
    
## <a name="see-also"></a>関連項目



[Outlookアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造](stream-structures.md)
  
[FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)
  
[FirstSkipBlockContent ストリーム構造](firstskipblockcontent-stream-structure.md)

