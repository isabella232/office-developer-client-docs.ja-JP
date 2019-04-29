---
title: folderuserfields ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433977"
---
# <a name="folderuserfields-stream-sample"></a>folderuserfields ストリームのサンプル

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、folderuserfields ストリームの例について説明します。 stream には、 `TextField1`ユーザー定義フィールドの定義が含まれています。 この型は**テキスト**であり、folderuserfields ストリームには、folderuserfields ansi と folderuserfields の両方の unicode パーツが含まれています。 詳細については、「[フォルダーフィールドストリームの構造](folder-fields-stream-structures.md)」を参照してください。
  
## <a name="data-dump"></a>データダンプ

次に示すのは、バイナリエディターに表示されるストリームのデータダンプです。
  
|ストリームオフセット|データバイト|ASCII データ|
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
   

次に、 **folderuserfields**ストリームのサンプルデータを解析します。
  
- folderuserフィールド ansi: Offset 0x0。
    
  - fielddefinitioncount: Offset 0x0、4バイト: 0x00000002 (2)。
    
  - fielddefinitions: Offset 0x4、配列 2 folderfielddefinitiona streams。
    
    **最初の配列要素**:
    
    - FieldType: Offset 0x4、4バイト: 0x00000001 (ftstring)。
      
    - FieldNameLength: オフセット0x8、2バイト: 0x000a (10)
      
    - FieldName: オフセット0xa、10文字の配列。 ANSI 文字列の値: "TextField1"。
      
    - Common: Offset 0x14。
    
      - propsetguid: Offset 0x14, 16 バイト: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。
        
      - fcapm: Offset 0x24、4バイト: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)
        
      - dwstring: Offset 0x28、4バイト: 0x00000000。
        
      - dwbitmap: Offset 0x2C、4バイト: 0x00000000。
        
      - dwdisplay: Offset 0x30、4バイト: 0x00000000。
        
      - ifmt: オフセット0x34、4バイト: 0x00000000。
        
      - wszFormulaLength: オフセット0x38、2バイト: 0x0000 (0)。
        
      - wszFormula: オフセット0x3a、0 wchars の配列。 空の文字列値。
    
    **2 番目の配列要素**:
    
    - FieldType: オフセット0x3a、4バイト: 0x00000000 (ftnone)。
      
    - FieldNameLength: オフセット0x3e、2バイト: 0x0000 (0)。
      
    - FieldName: オフセット0x40、0文字の配列。 空の文字列値。
      
    - Common: オフセット0x40。
    
      - propsetguid: Offset 0x40、16バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。
        
      - fcapm: オフセット0x50、4バイト: 0x00000000 (0)。
        
      - dwstring: Offset 0x54、4バイト: 0x00000000。
        
      - dwbitmap: Offset 0x58、4バイト: 0x00000000。
        
      - dwdisplay: Offset 0x5C、4バイト: 0x00000000。
        
      - ifmt: オフセット0x60、4バイト: 0x00000000。
        
      - wszFormulaLength: Offset 0x64、2バイト: 0x0000 (0)。
        
      - wszFormula: オフセット0x66、0 wchars の配列。 空の文字列値。
    
- folderuserフィールド unicode: Offset 0x66。
    
  - fielddefinitioncount: Offset 0x66、4バイト: 0x00000002 (2)。
    
  - fielddefinitions: Offset 0x6a、配列 2 folderfielddefinitionw streams。
    
    **最初の配列要素**:
    
    - FieldType: Offset 0x6a、4バイト: 0x00000001 (ftstring)。
      
    - FieldNameLength: オフセット0x6e、2バイト: 0x000a (10)。
      
    - FieldName: Offset 0x70、10の wchars の配列。 Unicode 文字列値: "TextField1"。
      
    - Common: オフセット0x84。
    
      - propsetguid: Offset 0x84、16バイト: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。
        
      - fcapm: オフセット0x94、4バイト: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)
        
      - dwstring: Offset 0x98、4バイト: 0x00000000。
        
      - dwbitmap: オフセット0x9c、4バイト: 0x00000000。
        
      - dwdisplay: Offset 0xa0、4バイト: 0x00000000。
        
      - ifmt: Offset 0xa4、4バイト: 0x00000000。
        
      - wszFormulaLength: Offset 0xa8、2バイト: 0x0000 (0)。
        
      - wszFormula: Offset 0xaa、配列 0 wchars。 空の文字列値。
    
    **2 番目の配列要素**:
    
    - FieldType: Offset 0xaa、4バイト: 0x00000000 (ftnone)。
      
    - FieldNameLength: Offset 0xae、2バイト: 0x0000 (0)。
      
    - FieldName: オフセット0xb0、0 wchars の配列。 空の文字列値。
      
    - Common: オフセット0xb0。
    
      - propsetguid: Offset 0xb0、16バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。
        
      - fcapm: Offset 0xC0、4バイト: 0x00000000 (0)。
        
      - dwstring: Offset 0xc4、4バイト: 0x00000000。
        
      - dwbitmap: Offset 0xc8、4バイト: 0x00000000。
        
      - dwdisplay: Offset 0xcc、4バイト: 0x00000000。
        
      - ifmt: Offset 0xD0、4バイト: 0x00000000。
        
      - wszFormulaLength: Offset 0xD4、2バイト: 0x0000 (0)。
        
      - wszFormula: Offset 0xD6、0 wchars の配列。 空の文字列値。
    
## <a name="see-also"></a>関連項目

- [Outlook のアイテムとフィールド](outlook-items-and-fields.md)
- [propertydefinition ストリームの構造](propertydefinition-stream-structure.md)
- [fielddefinition ストリームの構造](fielddefinition-stream-structure.md)
- [skipblock ストリームの構造](skipblock-stream-structure.md)
- [firstskipblockcontent ストリームの構造](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString Stream 構造](packedansistring-stream-structure.md)
- [PackedUnicodeString Stream 構造](packedunicodestring-stream-structure.md)

