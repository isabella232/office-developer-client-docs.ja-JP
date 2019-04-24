---
title: PidLidAppointmentReplyName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356043"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a>PidLidAppointmentReplyName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会議出席依頼または会議の更新オブジェクトに最後に応答したユーザーを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptReplyName  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008230  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、代理人が応答した場合にのみ委任者に対して設定されます。 この値は、代理人のストアの**PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) プロパティと同じです。 このプロパティは、開催者には意味がありません。 **PR_MAILBOX_OWNER_NAME**の詳細については、「 [OXCSTOR](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)」で指定されている store オブジェクトプロトコルを参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> データ型定義を提供します。
    
[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

