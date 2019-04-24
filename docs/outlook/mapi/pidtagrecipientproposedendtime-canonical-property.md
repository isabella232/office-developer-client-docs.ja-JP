---
title: PidTagRecipientProposedEndTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332775"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a>PidTagRecipientProposedEndTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会議の終了時刻の提案を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_PROPOSEDENDTIME  <br/> |
|識別子:  <br/> |0x5fe4  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |トランスポート受信者  <br/> |
   
## <a name="remarks"></a>解説

**PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) プロパティの値が TRUE に設定されている場合、このプロパティの値は出席者が要求した値を**dispidApptEndWhole**の値として設定することを示します ([](pidlidappointmentendwhole-canonical-property.md)単一インスタンスの会議オブジェクトまたは exception オブジェクトの PidLidAppointmentEndWhole) プロパティ。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

