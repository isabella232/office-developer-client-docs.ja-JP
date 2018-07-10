---
title: PidLidAppointmentMessageClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8777b2119e6beefc4d69dc0babfc8672df3a468b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801730"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a>PidLidAppointmentMessageClass の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
会議出席依頼から生成される会議の**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidApptMessageClass  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000024  <br/> |
|データを入力します。  <br/> |PT_TSTRING  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値は"IPM をする必要がありますか.予定""IPM に付けられますか.予定。"です。 このプロパティが必要ではありません。
  
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
