---
title: PackedUnicodeString Stream 構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422615"
---
# <a name="packedunicodestring-stream-structure"></a>PackedUnicodeString Stream 構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PackedUnicodeString stream 構造体には、文字列の Unicode (utf-16) 表現が含まれています。 この文字列は、null 文字で終了していません。 このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。 実際に存在するデータ要素は、utf-16 形式の文字列の長さによって決まります。
  
- utf-16 形式の wchars が255未満の文字列の場合、データ要素は次のようになります。
    
  - 長さ: バイト (1 バイト)。文字列の utf-16 形式の wchars の長さ。 (バイト数)。
    
  - 文字: WCHAR の配列。 この配列の数は、Length data 要素と同じです。 配列内のデータは、文字列を utf-16 で表現したものです。
    
- utf-16 形式の 255 ~ 65535 wchars を含む文字列の場合、データ要素は次のようになります。
    
  - プレフィックス: BYTE (1 バイト)、255 (0xff) の値。
    
  - 長さ: WORD (2 バイト)。文字列の utf-16 形式の wchars の長さ。 (2 バイト) を指定します。
    
  - 文字: WCHAR の配列。 この配列の数は、Length data 要素と同じです。 配列内のデータは、文字列を utf-16 で表現したものです。
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造体](stream-structures.md)
  
[fielddefinition ストリームの構造](fielddefinition-stream-structure.md)

