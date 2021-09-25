---
title: FolderUserFields ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eed1ad0e1f64af5bf07cc0ca3c842eed10c43c47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561790"
---
# <a name="folderuserfields-stream-sample"></a>FolderUserFields ストリームのサンプル

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、FolderUserFields ストリームの例について説明します。 ストリームには、ユーザー定義フィールドの定義が含まれます  `TextField1` 。 型は **Text** で、FolderUserFields ストリームには FolderUserFieldsAnsi と FolderUserFieldsUnicode パーツの両方が含まれます。 詳細については、「Folder [Fields Stream Structures」を参照してください](folder-fields-stream-structures.md)。
  
## <a name="data-dump"></a>データ ダンプ

バイナリ エディターに表示されるストリームのデータ ダンプを次に示します。
  
|ストリーム のオフセット|データ バイト|ASCII データ|
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
   

**FolderUserFields** ストリームのサンプル データの解析を次に示します。
  
- FolderUserFieldsAnsi: オフセット 0x0。
    
  - FieldDefinitionCount: オフセット 0x0、4 バイト: 0x00000002 (2) です。
    
  - FieldDefinitions: Offset 0x4、2 つの FolderFieldDefinitionA ストリームの配列。
    
    **最初の配列要素**:
    
    - FieldType: オフセット 0x4、4 バイト: 0x00000001 (ftString)。
      
    - FieldNameLength: オフセット 0x8、2 バイト: 0x000A (10)
      
    - FieldName: オフセット0xA、10 の CHARs の配列です。 ANSI 文字列値: "TextField1"
      
    - 共通: オフセット0x14。
    
      - PropSetGuid: オフセット 0x14、16 バイト: {00020329-00000-0000-C000-0000-0000000046} (PS_PUBLIC_STRINGS)。
        
      - fcapm: オフセット 0x24、4 バイト: 0x80000007 (FCAPM_CAN_EDIT|FCAPM_CAN_SORT|FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM)。
        
      - dwString: オフセット 0x28、4 バイト: 0x00000000。
        
      - dwBitmap: オフセット 0x2C、4 バイト: 0x00000000。
        
      - dwDisplay: オフセット 0x30、4 バイト: 0x00000000。
        
      - iFmt: オフセット0x34、4 バイト: 0x00000000。
        
      - wszFormulaLength: オフセット 0x38、2 バイト: 0x0000 (0) です。
        
      - wszFormula: オフセット0x3A 0 WCHARs の配列です。 空の文字列値。
    
    **2 番目の配列要素**:
    
    - FieldType: オフセット 0x3A、4 バイト: 0x00000000 (ftNone)。
      
    - FieldNameLength: オフセット 0x3E、2 バイト: 0x0000 (0) です。
      
    - FieldName: オフセット0x40、0 の CHARs の配列です。 空の文字列値。
      
    - 共通: オフセット0x40。
    
      - PropSetGuid: オフセット 0x40、16 バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。
        
      - fcapm: オフセット 0x50、4 バイト: 0x00000000 (0)。
        
      - dwString: オフセット 0x54、4 バイト: 0x00000000。
        
      - dwBitmap: オフセット 0x58、4 バイト: 0x00000000。
        
      - dwDisplay: オフセット 0x5C、4 バイト: 0x00000000。
        
      - iFmt: オフセット0x60、4 バイト: 0x00000000。
        
      - wszFormulaLength: オフセット 0x64、2 バイト: 0x0000 (0) です。
        
      - wszFormula: オフセット0x66 0 WCHARs の配列です。 空の文字列値。
    
- FolderUserFieldsUnicode: オフセット0x66。
    
  - FieldDefinitionCount: オフセット 0x66、4 バイト: 0x00000002 (2)。
    
  - FieldDefinitions: Offset 0x6A、2 つの FolderFieldDefinitionW ストリームの配列。
    
    **最初の配列要素**:
    
    - FieldType: オフセット 0x6A、4 バイト: 0x00000001 (ftString)。
      
    - FieldNameLength: オフセット 0x6E、2 バイト: 0x000A (10)。
      
    - FieldName: オフセット0x70 10 WCHARs の配列です。 Unicode 文字列値: "TextField1"
      
    - 共通: オフセット0x84。
    
      - PropSetGuid: オフセット 0x84、16 バイト: {00020329-00000-00000-C0000-0000000046} (PS_PUBLIC_STRINGS)。
        
      - fcapm: オフセット 0x94、4 バイト: 0x80000007 (FCAPM_CAN_EDIT|FCAPM_CAN_SORT|FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM)。
        
      - dwString: オフセット 0x98、4 バイト: 0x00000000。
        
      - dwBitmap: オフセット 0x9C、4 バイト: 0x00000000。
        
      - dwDisplay: オフセット 0xA0、4 バイト: 0x00000000。
        
      - iFmt: オフセット 0xA4、4 バイト: 0x00000000。
        
      - wszFormulaLength: オフセット 0xA8、2 バイト: 0x0000 (0)。
        
      - wszFormula: オフセット0xAA 0 WCHARs の配列です。 空の文字列値。
    
    **2 番目の配列要素**:
    
    - FieldType: オフセット 0xAA、4 バイト: 0x00000000 (ftNone)。
      
    - FieldNameLength: オフセット 0xAE、2 バイト: 0x0000 (0) です。
      
    - FieldName: オフセット0xB0 0 WCHARs の配列です。 空の文字列値。
      
    - 共通: オフセット0xB0。
    
      - PropSetGuid: オフセット 0xB0、16 バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。
        
      - fcapm: オフセット 0xC0、4 バイト: 0x00000000 (0)。
        
      - dwString: オフセット 0xC4、4 バイト: 0x00000000。
        
      - dwBitmap: オフセット 0xC8、4 バイト: 0x00000000。
        
      - dwDisplay: オフセット 0xCC、4 バイト: 0x00000000。
        
      - iFmt: オフセット 0xD0、4 バイト: 0x00000000。
        
      - wszFormulaLength: オフセット 0xD4、2 バイト: 0x0000 (0) です。
        
      - wszFormula: オフセット0xD6 0 WCHARs の配列です。 空の文字列値。
    
## <a name="see-also"></a>関連項目

- [Outlookアイテムとフィールド](outlook-items-and-fields.md)
- [PropertyDefinition ストリーム構造](propertydefinition-stream-structure.md)
- [FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)
- [SkipBlock ストリーム構造](skipblock-stream-structure.md)
- [FirstSkipBlockContent ストリーム構造](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString ストリーム構造](packedansistring-stream-structure.md)
- [PackedUnicodeString ストリーム構造](packedunicodestring-stream-structure.md)

