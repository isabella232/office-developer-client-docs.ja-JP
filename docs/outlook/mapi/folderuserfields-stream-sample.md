---
title: FolderUserFields ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800079"
---
# <a name="folderuserfields-stream-sample"></a>FolderUserFields ストリームのサンプル

**適用対象**: Outlook 
  
このトピックでは、FolderUserFields ストリームの例について説明します。 ストリームには、ユーザー定義のフィールドの定義が含まれている`TextField1`。 型は、**テキスト**、および FolderUserFields ストリームには、FolderUserFieldsAnsi と FolderUserFieldsUnicode の両方のパーツが含まれています。 詳細については、[フォルダー フィールドのストリームの構造体](folder-fields-stream-structures.md)を参照してください。
  
## <a name="data-dump"></a>データのダンプ

次のストリームのデータのダンプがバイナリ エディターで表示します。
  
|ストリームのオフセット|データのバイト数|ASCII データ|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

**FolderUserFields**ストリームのサンプル データの解析は、次のようにします。
  
- FolderUserFieldsAnsi: はオフセット 0x0 です。
    
  - FieldDefinitionCount: 0x0 では、4 バイトのオフセット: 0x00000002 (2)。
    
  - FieldDefinitions: オフセット 0x4、2 つの FolderFieldDefinitionA ストリームの配列。
    
    **配列の最初の要素**。
    
    - FieldType: 0x4、4 バイトのオフセット: 0x00000001 (ftString)。
      
    - FieldNameLength: 0x8、2 バイトのオフセット: 0x000A (10)
      
    - フィールド名: オフセット 0 xa は、10 文字の配列です。 ANSI 文字列の値:「TextField1」です。
      
    - 共通: 0x14 をオフセットします。
    
      - PropSetGuid: 0x14、16 バイトのオフセット: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。
        
      - fcapm: 0x24、4 バイトのオフセット: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)。
        
      - dwString: 4 バイト目の 0x28 にオフセット: 0x00000000 です。
        
      - dwBitmap: 0x2C、4 バイトのオフセット: 0x00000000 です。
        
      - dwDisplay: 0x30、4 バイトのオフセット: 0x00000000 です。
        
      - iFmt: 0x34, 4 バイトのオフセット: 0x00000000 です。
        
      - wszFormulaLength: 0x38 は、2 バイトのオフセット: 0x0000 (0)。
        
      - wszFormula: 0x3A、WCHARs が 0 の配列のオフセット。 空の文字列値です。
    
    **2 番目の配列要素**。
    
    - FieldType: 0x3A、4 バイトのオフセット: 0x00000000 (ftNone)。
      
    - FieldNameLength: 0x3E、2 バイトのオフセット: 0x0000 (0)。
      
    - フィールド名: オフセット 0x40、文字数が 0 の配列です。 空の文字列値です。
      
    - オフセット 0x40 の一般的な: です。
    
      - PropSetGuid: 0x40、16 バイトのオフセット: {00000000-0000-0000-0000-000000000000} (GUID_)。
        
      - fcapm: 0x50、4 バイトのオフセット: 0x00000000 (0)。
        
      - dwString: 0x54、4 バイトのオフセット: 0x00000000 です。
        
      - dwBitmap: 0x58、4 バイトのオフセット: 0x00000000 です。
        
      - dwDisplay: 0x5C、4 バイトのオフセット: 0x00000000 です。
        
      - iFmt: 0x60、4 バイトのオフセット: 0x00000000 です。
        
      - wszFormulaLength: 0x64、2 バイトのオフセット: 0x0000 (0)。
        
      - wszFormula: 0x66、WCHARs が 0 の配列のオフセット。 空の文字列値です。
    
- FolderUserFieldsUnicode: 0x66 をオフセットします。
    
  - FieldDefinitionCount: 0x66、4 バイトのオフセット: 0x00000002 (2)。
    
  - FieldDefinitions: 0x6A、FolderFieldDefinitionW の 2 つのストリームの配列をオフセットします。
    
    **配列の最初の要素**。
    
    - FieldType: 0x6A、4 バイトのオフセット: 0x00000001 (ftString)。
      
    - FieldNameLength: 0x6E、2 バイトのオフセット: 0x000A (10)。
      
    - フィールド名: 0x70、10 WCHARs の配列のオフセットします。 Unicode 文字列の値:「TextField1」です。
      
    - 0x84: 共通のオフセットです。
    
      - PropSetGuid: 次の 16 バイトのオフセット: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。
        
      - fcapm: 0x94、4 バイトのオフセット: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)。
        
      - dwString: 0x98、4 バイトのオフセット: 0x00000000 です。
        
      - dwBitmap: 0x9C、4 バイトのオフセット: 0x00000000 です。
        
      - dwDisplay: 0xa0 にある、4 バイトのオフセット: 0x00000000 です。
        
      - iFmt: 0xA4、4 バイトのオフセット: 0x00000000 です。
        
      - wszFormulaLength: 0xA8、2 バイトのオフセット: 0x0000 (0)。
        
      - wszFormula: 0xAA、WCHARs が 0 の配列のオフセット。 空の文字列値です。
    
    **2 番目の配列要素**。
    
    - FieldType: 0xAA、4 バイトのオフセット: 0x00000000 (ftNone)。
      
    - FieldNameLength: 0xAE、2 バイトのオフセット: 0x0000 (0)。
      
    - フィールド名: 0xB0、WCHARs が 0 の配列をオフセットします。 空の文字列値です。
      
    - 0xB0: 共通のオフセットです。
    
      - PropSetGuid: 0xB0、16 バイトのオフセット: {00000000-0000-0000-0000-000000000000} (GUID_)。
        
      - fcapm: 0xC0、4 バイトのオフセット: 0x00000000 (0)。
        
      - dwString: 0xC4、4 バイトのオフセット: 0x00000000 です。
        
      - dwBitmap: 0xC8、4 バイトのオフセット: 0x00000000 です。
        
      - dwDisplay: 0xCC、4 バイトのオフセット: 0x00000000 です。
        
      - iFmt: 0xD0、4 バイトのオフセット: 0x00000000 です。
        
      - wszFormulaLength: 0xD4、2 バイトのオフセット: 0x0000 (0)。
        
      - wszFormula: ように WCHARs が 0 の配列のオフセット。 空の文字列値です。
    
## <a name="see-also"></a>関連項目

- [Outlook のアイテムとフィールド](outlook-items-and-fields.md)
- [PropertyDefinition ストリームの構造](propertydefinition-stream-structure.md)
- [FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)
- [SkipBlock ストリームの構造](skipblock-stream-structure.md)
- [FirstSkipBlockContent ストリームの構造](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString ストリームの構造](packedansistring-stream-structure.md)
- [PackedUnicodeString ストリームの構造](packedunicodestring-stream-structure.md)

