---
title: PidLidNoteColor の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7ff0bb5ec1eb56724bee7be7dec13f0474711083
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802050"
---
# <a name="pidlidnotecolor-canonical-property"></a>PidLidNoteColor の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メモの推奨の背景色を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidNoteColor  <br/> |
|プロパティを設定します。  <br/> |PSETID_Note  <br/> |
|長い ID (LID):  <br/> |0x00008B00  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |付箋  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
