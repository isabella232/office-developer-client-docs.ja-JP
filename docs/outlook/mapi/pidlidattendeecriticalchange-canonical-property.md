---
title: PidLidAttendeeCriticalChange の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAttendeeCriticalChange
api_type:
- COM
ms.assetid: 2b46966d-c63d-4241-92d4-001d6a674e97
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f534a4738eb18519dc62cc18cfb79391ea39633b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801824"
---
# <a name="pidlidattendeecriticalchange-canonical-property"></a>PidLidAttendeeCriticalChange の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
会議に関連するオブジェクトが送信されたときの日時を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |LID_ATTENDEE_CRITICAL_CHANGE  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000001  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

値は、世界協定時刻 (UTC) で指定する必要があります。
  
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

