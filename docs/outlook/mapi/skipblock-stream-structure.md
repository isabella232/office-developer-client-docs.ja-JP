---
title: skipblock ストリームの構造
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
# <a name="skipblock-stream-structure"></a>skipblock ストリームの構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
skipblock ストリーム構造は、ブロックの残りの部分の長さを指定する整数で始まるデータのブロックです。 このストリーム構造は、フィールド定義が PropDefV2 形式である場合に、 [fielddefinition](fielddefinition-stream-structure.md)ストリーム内に存在します。 
  
skipblock ストリーム構造の目的は、fielddefinition stream の skipblock data 要素内の一連の like 構造での相対的な位置に依存します。 skipblocks シリーズには、データ系列を終了し、Size data 要素が0である skipblocks 構造が少なくとも1つ含まれている必要があります。 最初の構造が終端構造ではない場合 (つまり、Size data 要素が0より大きい場合)、Outlook は最初の構造体が Unicode (utf-16) でフィールド名を指定しているものとします。
  
このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。
  
- size: data data 要素のバイト単位での DWORD (4 バイト) です。
    
- コンテンツ: バイトの配列。 この配列の数は、Size data 要素と同じです。 Content data 要素の意味は、Outlook のデータ系列とバージョンの skipblock 構造体の場所によって異なります。 最初の skipblock 構造が終了構造ではない場合、Outlook は最初の skipblock 構造を、Unicode でフィールド名を指定する[firstskipblockcontent](firstskipblockcontent-stream-structure.md)ストリーム構造体と見なします。 
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造体](stream-structures.md)
  
[fielddefinition ストリームの構造](fielddefinition-stream-structure.md)
  
[firstskipblockcontent ストリームの構造](firstskipblockcontent-stream-structure.md)

