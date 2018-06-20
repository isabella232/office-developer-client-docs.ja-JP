---
title: PidLidWhere の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 127627b79782a2a785b00b79b9940b66256a08eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802294"
---
# <a name="pidlidwhere-canonical-property"></a>PidLidWhere の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
イベントの場所を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |LID_WHERE  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000002  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値は、関連付けられている会議から**dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値と同じはずです。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

