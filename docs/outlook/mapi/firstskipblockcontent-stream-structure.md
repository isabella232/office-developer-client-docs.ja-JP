---
title: firstskipblockcontent ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 89814eec-67c1-40b6-91d9-a58c3da0f15e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4804f2c6633095ea9eb38bec990cb1554240f6e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433928"
---
# <a name="firstskipblockcontent-stream-structure"></a>firstskipblockcontent ストリームの構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
firstskipblockcontent ストリーム構造は、 [fielddefinition](fielddefinition-stream-structure.md)ストリームの skipblocks データ要素の最初の[skipblock](skipblock-stream-structure.md)構造体の内容です。 firstskipblockcontent ストリームは単なる data 要素である FieldName、次のようになります。 
  
- FieldName: [PackedUnicodeString](packedunicodestring-stream-structure.md)。フィールド名を指定します。
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造体](stream-structures.md)
  
[skipblock ストリームの構造](skipblock-stream-structure.md)
  
[PackedUnicodeString Stream 構造](packedunicodestring-stream-structure.md)

