---
title: PidLidNoteColor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNoteColor
api_type:
- COM
ms.assetid: 9d4b8f5f-1789-497c-8010-f83da9ba5966
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7fd41f46adf9b7d9aa3b48779b03cd6936a5fb5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583135"
---
# <a name="pidlidnotecolor-canonical-property"></a>PidLidNoteColor 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メモの推奨の背景色を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidNoteColor  <br/> |
|プロパティを設定します。  <br/> |PSETID_Note  <br/> |
|長い ID (LID):  <br/> |0x00008B00  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |付箋  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次の表のエントリのいずれかを使用する必要があります。
  
|**値**|**色**|
|:-----|:-----|
|0x00000000  <br/> |青  <br/> |
|0x00000001  <br/> |緑  <br/> |
|0x00000002  <br/> |ピンク  <br/> |
|0x00000003  <br/> |黄  <br/> |
|0x00000004  <br/> |白  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXONOTE]](http://msdn.microsoft.com/library/6bf4ed7e-316c-4a3c-be27-5ec93e7ab39f%28Office.15%29.aspx)
  
> プロパティとは、ノートの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

