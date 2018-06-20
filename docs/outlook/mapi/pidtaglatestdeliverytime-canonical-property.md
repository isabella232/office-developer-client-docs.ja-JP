---
title: PidTagLatestDeliveryTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802933"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>PidTagLatestDeliveryTime の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
最新の日付と時刻のメッセージ転送エージェント (MTA) がメッセージを配信する場合が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_LATEST_DELIVERY_TIME  <br/> |
|識別子:  <br/> |0x0019  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

MTA は、このプロパティは、指定の時間でメッセージを配信することはできません、する場合は、メッセージを配信せずをキャンセルします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

