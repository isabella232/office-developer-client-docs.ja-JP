---
title: PackedUnicodeString ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569198"
---
# <a name="packedunicodestring-stream-structure"></a>PackedUnicodeString ストリームの構造

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PackedUnicodeString ストリームの構造体には、Unicode (utf-16) 形式文字列にはが含まれています。 この文字列は null 文字で終了していません。 このストリーム内のデータ要素は、以下に示す順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。 存在する実際のデータ要素は、utf-16 形式で文字列の長さによって異なります。
  
- Utf-16 形式には、255 バイト未満の WCHARs が含まれている文字列のデータ要素は次のとおりです。
    
  - 長さ: バイト (1 バイト)、utf-16 文字列表現の長さ、WCHARs の数です。
    
  - 文字: wchar 型の配列。 この配列は長さのデータ要素になります。 配列内のデータは、文字列の utf-16 表現です。
    
- Utf-16 形式には、255 ~ 65535 WCHARs が含まれている文字列のデータ要素は次のとおりです。
    
  - プレフィックス: バイト (1 バイト) で、値の 255 (0 xff) です。
    
  - 長さ: ワード (2 バイト)、utf-16 文字列表現の長さ、WCHARs、数です。
    
  - 文字: wchar 型の配列。 この配列は長さのデータ要素になります。 配列内のデータは、文字列の utf-16 表現です。
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[ストリームの構造](stream-structures.md)
  
[FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)

