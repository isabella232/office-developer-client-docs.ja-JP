---
title: PropertyDefinition ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803706"
---
# <a name="propertydefinition-stream-sample"></a>PropertyDefinition ストリームのサンプル

**適用されます**: Outlook 
  
PropertyDefinition ストリームの例について説明します。 ストリームには、ユーザー定義のフィールドの定義が含まれている`TextField1`。 型は、**テキスト**、および PropDefV2 の形式では、定義します。
  
## <a name="data-dump"></a>データのダンプ

次のストリームのデータのダンプがバイナリ エディターで表示します。
  
|ストリームのオフセット|データのバイト数|ASCII データ|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
PropertyDefinition ストリームのサンプル データの解析は、次のようにします。
  
- バージョン: 0x0 では、2 バイトのオフセット: 0x0103 (PropDefV2)。
    
- FieldDefinitionCount: 0x2、4 バイトのオフセット: 0x1 (1)。
    
- FieldDefinitions: 0x6、1 の FieldDefinition ストリームの配列をオフセットします。
    
  - フラグ: 0x6、4 バイトのオフセット: 0x45 (PDO_IS_CUSTOM |PDO_PRINT_SAVEAS |PDO_PRINT_SAVEAS_DEF)。
    
  - VT: オフセットの 2 バイトの 0 xa: 0x8 (**VT_BSTR**)。
    
  - DispId: 0 xc、4 バイトのオフセット: 0x0 (0)。
    
  - NmidNameLength: 0x10、2 バイトのオフセット: 0 xa (10)。
    
  - NmidName: 0x12, WCHARs が 10 の配列のオフセットします。 Unicode 文字列の値:「TextField1」です。
    
  - NameANSI: 0x26、PackedAnsiString ストリームをオフセットします。
    
    - 長さ: オフセット 0x26、1 バイト: 0 xa (10)。
      
    - 文字: 0x27、10 文字の配列をオフセットします。 ANSI 文字列の値:「TextField1」です。
    
  - FormulaANSI: オフセットれました、PackedAnsiString のストリーム。
    
    - 長さ: オフセットれました、1 バイト: 0x0 (0)。
      
    - 文字: 0x32、0 文字の配列をオフセットします。 空の ANSI 文字列。
    
  - ValidationRuleANSI: 0x32、PackedAnsiString ストリームをオフセットします。
    
    - 長さ: オフセット 0x32、1 バイト: 0x0 (0)。
      
    - 文字: 0x33、0 文字の配列をオフセットします。 空の ANSI 文字列。
    
  - ValidationTextANSI: 0x33、PackedAnsiString ストリームをオフセットします。
    
    - 長さ: オフセット 0x33、1 バイト: 0x0 (0)。
      
    - 文字: は、0x34, 0 の文字の配列をオフセットします。 空の ANSI 文字列。
    
  - ErrorANSI: 0x34, PackedAnsiString ストリームをオフセットします。
    
    - 長さ: オフセット 0x34, 1 バイト: 0x0 (0)。
      
    - 文字: 0x35、文字数が 0 の配列のオフセットします。 空の ANSI 文字列。
    
  - InternalType: 0x35、4 バイトのオフセット: 0x0 (iTypeString)。
    
  - SkipBlocks: 0x39、一連の SkipBlock ストリームのオフセットします。
    
  - 最初の SkipBlock
    
    - サイズ: 0x39、4 バイトのオフセット: 0x15 (21)。
      
    - コンテンツ: 0x3D、21 のバイト配列をオフセットします。 これは最初の SkipBlock ストリームでは、この配列には、FirstSkipBlockContent ストリームが含まれています。
      
      - フィールド名: 0x3D、PackedUnicodeString ストリームをオフセットします。
        
        - 長さ: オフセット 0x3D、1 バイト: 0 xa (10)。
          
        - 文字: オフセット 0x3E、WCHARs の 10 個の配列です。 Unicode 文字列の値:「TextField1」です。
    
  - 2 番目の SkipBlock
    
    - サイズ: 使用、4 バイトのオフセット: 0x0 (0)。 これは、終端の SkipBlock ストリームです。
    
## <a name="see-also"></a>関連項目

- [Outlook アイテムおよびフィールド](outlook-items-and-fields.md)
- [ストリームの構造](stream-structures.md)
- [PropertyDefinition ストリームの構造](propertydefinition-stream-structure.md)
- [FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)
- [SkipBlock ストリームの構造](skipblock-stream-structure.md)
- [FirstSkipBlockContent ストリームの構造](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString ストリームの構造](packedansistring-stream-structure.md)
- [PackedUnicodeString ストリームの構造](packedunicodestring-stream-structure.md)

