---
title: PackedAnsiString ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4e919270efb196cda845581830cc4a918012b385
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578977"
---
# <a name="packedansistring-stream-structure"></a>PackedAnsiString ストリームの構造

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PackedAnsiString ストリームの構造体には、ANSI 形式 Microsoft Outlook を実行しているコンピューターの ANSI コード ページに基づいて、文字列にはが含まれています。 この文字列は null 文字で終了していません。 このストリーム内のデータ要素は、以下に示す順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。 存在する実際のデータ要素は、ANSI 形式の文字列の長さによって異なります。
  
- ANSI 形式には、255 バイト未満の場合が含まれている文字列のデータ要素は次のとおりです。
    
  - 長さ: バイト (1 バイト) で、ANSI 文字列表現の長さをバイト数で。
    
  - 文字: 文字の配列。 この配列は長さのデータ要素になります。 配列内のデータは、文字列の ANSI 形式です。
    
- ANSI 形式には、255 ~ 65535 バイトが含まれている文字列のデータ要素は次のとおりです。
    
  - プレフィックス: バイト (1 バイト) で、値の 255 (0 xff) です。
    
  - 長さ: ワード (2 バイト) で、ANSI 文字列表現の長さをバイト数で。
    
  - 文字: 文字の配列。 この配列は長さのデータ要素になります。 配列内のデータは、文字列の ANSI 形式です。
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[ストリームの構造](stream-structures.md)
  
[FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)

