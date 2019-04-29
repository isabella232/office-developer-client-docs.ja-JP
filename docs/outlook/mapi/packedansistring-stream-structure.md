---
title: PackedAnsiString Stream 構造
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
# <a name="packedansistring-stream-structure"></a>PackedAnsiString Stream 構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PackedAnsiString stream 構造体には、Microsoft Outlook が実行されているコンピューターの ansi コードページに基づいて、文字列の ansi 表現が含まれています。 この文字列は、null 文字で終了していません。 このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。 実際に存在するデータ要素は、ANSI 表現の文字列の長さによって決まります。
  
- ANSI 表現が255バイト未満の文字列の場合、データ要素は次のようになります。
    
  - length: BYTE (1 バイト) (バイト数)。文字列の ANSI 表現の長さ。
    
  - 文字: CHAR の配列。 この配列の数は、Length data 要素と同じです。 配列内のデータは、文字列の ANSI 表現です。
    
- ANSI 表記に 255 ~ 65535 バイトの文字列が含まれている場合、データ要素は次のようになります。
    
  - プレフィックス: BYTE (1 バイト)、255 (0xff) の値。
    
  - length: WORD (2 バイト)。文字列の ANSI 表現の長さをバイト数で指定します。
    
  - 文字: CHAR の配列。 この配列の数は、Length data 要素と同じです。 配列内のデータは、文字列の ANSI 表現です。
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[Stream 構造体](stream-structures.md)
  
[fielddefinition ストリームの構造](fielddefinition-stream-structure.md)

