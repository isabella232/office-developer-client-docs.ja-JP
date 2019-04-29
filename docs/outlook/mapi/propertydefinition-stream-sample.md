---
title: propertydefinition ストリームのサンプル
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
# <a name="propertydefinition-stream-sample"></a>propertydefinition ストリームのサンプル

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、propertydefinition stream の例について説明します。 stream には、 `TextField1`ユーザー定義フィールドの定義が含まれています。 この型は**テキスト**であり、定義は PropDefV2 形式になっています。
  
## <a name="data-dump"></a>データダンプ

次に示すのは、バイナリエディターに表示されるストリームのデータダンプです。
  
|ストリームオフセット|データバイト|ASCII データ|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
次に、propertydefinition ストリームのサンプルデータを解析します。
  
- バージョン: Offset 0x0、2バイト: 0x0103 (PropDefV2)。
    
- fielddefinitioncount: Offset 0x2、4バイト: 0x1 (1)。
    
- fielddefinitions: Offset 0x6、1つの fielddefinitions stream の配列。
    
  - フラグ: オフセット0x6、4バイト: 0x45 (PDO_IS_CUSTOM |PDO_PRINT_SAVEAS |PDO_PRINT_SAVEAS_DEF)
    
  - VT: オフセット0xa、2バイト: 0x8 (**VT_BSTR**)。
    
  - DispId: Offset 0xC、4バイト: 0x0 (0)。
    
  - NmidNameLength: オフセット0x10、2バイト: 0xa (10)。
    
  - nmidname: Offset 0x12、10の wchars の配列。 Unicode 文字列値: "TextField1"。
    
  - nameansi: Offset 0x26, PackedAnsiString stream。
    
    - 長さ: Offset 0x26、1バイト: 0xa (10)。
      
    - 文字: Offset 0x27、10文字の配列。 ANSI 文字列の値: "TextField1"。
    
  - FormulaANSI: オフセット0x31、PackedAnsiString stream。
    
    - 長さ: オフセット0x31、1バイト: 0x0 (0)。
      
    - 文字: Offset 0x32、0文字の配列。 空の ANSI 文字列。
    
  - validationruleansi: Offset 0x32、PackedAnsiString stream。
    
    - 長さ: Offset 0x32、1バイト: 0x0 (0)。
      
    - 文字: Offset 0x33、0文字の配列。 空の ANSI 文字列。
    
  - validationtextansi: Offset 0x33, PackedAnsiString stream。
    
    - 長さ: Offset 0x33、1バイト: 0x0 (0)。
      
    - 文字: オフセット0x34、0文字の配列。 空の ANSI 文字列。
    
  - erroransi: オフセット0x34、PackedAnsiString stream。
    
    - 長さ: オフセット0x34、1バイト: 0x0 (0)。
      
    - 文字: Offset 0x35、0文字の配列。 空の ANSI 文字列。
    
  - internaltype: Offset 0x35、4バイト: 0x0 (iTypeString)。
    
  - skipblocks: オフセット0x39、一連の skipblocks ストリーム。
    
  - 最初の skipblock
    
    - サイズ: オフセット0x39、4バイト: 0x15 (21)。
      
    - コンテンツ: Offset 0x3d、配列21バイト。 これは最初の skipblock ストリームなので、この配列には firstskipblockcontent ストリームが含まれています。
      
      - FieldName: Offset 0x3d、PackedUnicodeString stream。
        
        - 長さ: Offset 0x3d、1バイト: 0xa (10)。
          
        - 文字: オフセット0x3e、10の wchars の配列。 Unicode 文字列値: "TextField1"。
    
  - 2番目の skipblock
    
    - サイズ: オフセット0x52、4バイト: 0x0 (0)。 これは、終了した skipblock ストリームです。
    
## <a name="see-also"></a>関連項目

- [Outlook のアイテムとフィールド](outlook-items-and-fields.md)
- [Stream 構造体](stream-structures.md)
- [propertydefinition ストリームの構造](propertydefinition-stream-structure.md)
- [fielddefinition ストリームの構造](fielddefinition-stream-structure.md)
- [skipblock ストリームの構造](skipblock-stream-structure.md)
- [firstskipblockcontent ストリームの構造](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString Stream 構造](packedansistring-stream-structure.md)
- [PackedUnicodeString Stream 構造](packedunicodestring-stream-structure.md)

