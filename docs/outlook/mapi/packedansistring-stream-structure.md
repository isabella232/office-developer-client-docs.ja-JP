---
title: PackedAnsiString ストリーム構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404506"
---
# <a name="packedansistring-stream-structure"></a>PackedAnsiString ストリーム構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PackedAnsiString ストリーム構造には、Microsoft が実行されているコンピューターの ANSI コード ページに基づいて、文字列の ANSI 表現Outlook含まれます。 この文字列は null 文字で終了されません。 このストリーム内のデータ要素は、次に示す順序で、お互いに直後に続く、リトル エンディアン バイト順に格納されます。 実際に存在するデータ要素は、ANSI 表現の文字列の長さによって異なっています。
  
- ANSI 表記が 255 バイト未満の文字列の場合、データ要素は次のとおりです。
    
  - 長さ: BYTE (1 バイト)、文字列の ANSI 表記の長さ (バイト数)。
    
  - 文字: CHAR の配列。 この配列の数は、Length データ要素と等しくなります。 配列内のデータは、文字列の ANSI 表記です。
    
- ANSI 表現に 255 ~ 65535 バイトが含まれる文字列の場合、データ要素は次のとおりです。
    
  - プレフィックス: BYTE (1 バイト)、値 255 (0xff)。
    
  - 長さ: 文字列の ANSI 表記の WORD (2 バイト)、長さ (バイト数)。
    
  - 文字: CHAR の配列。 この配列の数は、Length データ要素と等しくなります。 配列内のデータは、文字列の ANSI 表記です。
    
## <a name="see-also"></a>関連項目



[Outlookアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造](stream-structures.md)
  
[FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)

