---
title: SkipBlock ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803939"
---
# <a name="skipblock-stream-structure"></a>SkipBlock ストリームの構造

  
  
**適用対象**: Outlook 
  
SkipBlock ストリームの構造体は、ブロックの残りの部分の長さを指定する整数値で始まるデータのブロックです。 このストリームの構造体は、フィールド定義は、PropDefV2 形式の場合、 [FieldDefinition](fielddefinition-stream-structure.md)ストリームに存在します。 
  
SkipBlock ストリームの構造体の目的は、FieldDefinition ストリームの SkipBlocks のデータ要素の構造体のような一連の相対位置によって異なります。 SkipBlocks シリーズは、シリーズを終了し、0 に等しいサイズのデータ要素を持つことが少なくとも 1 つの SkipBlock 構造体を含める必要があります。 最初の構造は、終端の構造ではない場合 (つまり、サイズのデータ要素が 0 より大きい)、Outlook は、最初の構造体は、Unicode (utf-16) でフィールド名を指定します。
  
このストリーム内のデータ要素は、以下に指定した順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。
  
- サイズ: DWORD (4 バイト) で、サイズ、コンテンツのデータ要素のバイト単位の数。
    
- コンテンツ: バイトの配列。 この配列は、サイズのデータ要素と同じです。 コンテンツのデータ要素の意味は、一連の SkipBlock 構造体の場所や Outlook のバージョンによって異なります。 最初の SkipBlock 構造体が終端構造でない場合は、Outlook では Unicode でフィールド名を指定する[FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)ストリームの構造体として最初の SkipBlock 構造体が考慮されます。 
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[ストリームの構造](stream-structures.md)
  
[FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)
  
[FirstSkipBlockContent ストリームの構造](firstskipblockcontent-stream-structure.md)

