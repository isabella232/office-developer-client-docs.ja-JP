---
title: PropertyDefinition ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406662"
---
# <a name="propertydefinition-stream-sample"></a>PropertyDefinition ストリームのサンプル

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、PropertyDefinition ストリームの例について説明します。 ストリームには、ユーザー定義フィールドの定義が含まれます  `TextField1` 。 型は **Text** で、定義は PropDefV2 形式です。
  
## <a name="data-dump"></a>データ ダンプ

バイナリ エディターに表示されるストリームのデータ ダンプを次に示します。
  
|ストリーム のオフセット|データ バイト|ASCII データ|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
PropertyDefinition ストリームのサンプル データの解析を次に示します。
  
- バージョン: オフセット 0x0 2 バイト: 0x0103 (PropDefV2)。
    
- FieldDefinitionCount: オフセット 0x2、4 バイト: 0x1 (1)。
    
- FieldDefinitions: オフセット0x6、1 FieldDefinition ストリームの配列です。
    
  - フラグ: オフセット 0x6、4 バイト: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF)。
    
  - VT: オフセット 0xA、2 バイト: 0x8 **(** VT_BSTR)。
    
  - DispId: オフセット 0xC、4 バイト: 0x0 (0)。
    
  - NmidNameLength: オフセット 0x10、2 バイト: 0xA (10)。
    
  - NmidName: オフセット0x12 10 WCHARs の配列です。 Unicode 文字列値: "TextField1"
    
  - NameANSI: Offset 0x26 PackedAnsiString ストリーム。
    
    - 長さ: オフセット0x26、1 バイト: 0xA (10) です。
      
    - 文字: オフセット0x27、10 文字の配列です。 ANSI 文字列値: "TextField1"
    
  - FormulaANSI: Offset 0x31 PackedAnsiString ストリーム。
    
    - 長さ: オフセット0x31、1 バイト: 0x0 (0) です。
      
    - 文字: オフセット0x32、0 文字の配列です。 ANSI 文字列を空にします。
    
  - ValidationRuleANSI: Offset 0x32 PackedAnsiString ストリーム。
    
    - 長さ: オフセット0x32、1 バイト: 0x0 (0) です。
      
    - 文字: オフセット0x33、0 文字の配列です。 ANSI 文字列を空にします。
    
  - ValidationTextANSI: Offset 0x33 PackedAnsiString ストリーム。
    
    - 長さ: オフセット0x33、1 バイト: 0x0 (0) です。
      
    - 文字: オフセット0x34、0 文字の配列です。 ANSI 文字列を空にします。
    
  - ErrorANSI: Offset 0x34、PackedAnsiString ストリーム。
    
    - 長さ: オフセット0x34、1 バイト: 0x0 (0) です。
      
    - 文字: オフセット0x35、0 文字の配列です。 ANSI 文字列を空にします。
    
  - InternalType: Offset 0x35、4 バイト: 0x0 (iTypeString)。
    
  - SkipBlocks: 一連0x39一連の SkipBlock ストリームをオフセットします。
    
  - First SkipBlock
    
    - Size: Offset 0x39、4 バイト: 0x15 (21)。
      
    - コンテンツ: オフセット0x3D 21 バイトの配列。 これは最初の SkipBlock ストリームなので、この配列には FirstSkipBlockContent ストリームが含まれます。
      
      - FieldName: オフセット 0x3D PackedUnicodeString ストリーム。
        
        - 長さ: オフセット0x3D、1 バイト: 0xA (10)。
          
        - 文字: オフセット0x3E、10 WCHA の配列です。 Unicode 文字列値: "TextField1"
    
  - Second SkipBlock
    
    - Size: Offset 0x52、4 バイト: 0x0 (0)。 これは終了する SkipBlock ストリームです。
    
## <a name="see-also"></a>関連項目

- [Outlookアイテムとフィールド](outlook-items-and-fields.md)
- [Stream 構造](stream-structures.md)
- [PropertyDefinition ストリーム構造](propertydefinition-stream-structure.md)
- [FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)
- [SkipBlock ストリーム構造](skipblock-stream-structure.md)
- [FirstSkipBlockContent ストリーム構造](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString ストリーム構造](packedansistring-stream-structure.md)
- [PackedUnicodeString ストリーム構造](packedunicodestring-stream-structure.md)

