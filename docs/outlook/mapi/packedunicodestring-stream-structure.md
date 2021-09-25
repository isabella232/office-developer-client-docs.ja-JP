---
title: PackedUnicodeString ストリーム構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 73a3f6f8ca3dd23326f28ea18228c09cf310d444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625120"
---
# <a name="packedunicodestring-stream-structure"></a>PackedUnicodeString ストリーム構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PackedUnicodeString ストリーム構造には、文字列の Unicode (UTF-16) 表記が含まれます。 この文字列は null 文字で終了されません。 このストリーム内のデータ要素は、次に示す順序で、お互いに直後に続く、リトル エンディアン バイト順に格納されます。 実際に存在するデータ要素は、UTF-16 表記の文字列の長さに依存します。
  
- UTF-16 表記が 255 WCHA 未満の文字列の場合、データ要素は次のとおりです。
    
  - 長さ: BYTE (1 バイト)、文字列の UTF-16 表記の長さ (WCHARs の数)。
    
  - 文字: WCHAR の配列。 この配列の数は、Length データ要素と等しくなります。 配列内のデータは、文字列の UTF-16 表記です。
    
- UTF-16 表記に 255 ~ 65535 WCHA が含まれる文字列の場合、データ要素は次のとおりです。
    
  - プレフィックス: BYTE (1 バイト)、値 255 (0xff)。
    
  - 長さ: 文字列の UTF-16 表記の WORD (2 バイト)、WCHARs の数の長さ。
    
  - 文字: WCHAR の配列。 この配列の数は、Length データ要素と等しくなります。 配列内のデータは、文字列の UTF-16 表記です。
    
## <a name="see-also"></a>関連項目



[Outlookアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造](stream-structures.md)
  
[FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)

