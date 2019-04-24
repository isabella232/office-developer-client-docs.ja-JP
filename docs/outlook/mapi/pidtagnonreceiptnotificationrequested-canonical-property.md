---
title: PidTagNonReceiptNotificationRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329310"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>PidTagNonReceiptNotificationRequested 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信者が、指定された受信者に対して配信不能通知を要求している場合は、TRUE が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|識別子:  <br/> |0x0c06  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>解説

このプロパティに FALSE が含まれ、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティに TRUE が含まれている場合、サービスプロバイダーは**PR_NON_RECEIPT_NOTIFICATION_REQUESTED**プロパティを上書きし、配信不能レポート。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

