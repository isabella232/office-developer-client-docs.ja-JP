---
title: PidTagSpoolerStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348210"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>PidTagSpoolerStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーで使用可能な情報に基づいてメッセージの状態を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SPOOLER_STATUS  <br/> |
|識別子:  <br/> |0x0e10  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI ノンノンアウトテーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージオブジェクトの MAPI によって計算されます。
  
このプロパティは、受信メッセージのみに表示され、他のすべてのケースで予約されています。 メッセージが最終的な場所に配信されたかどうか、またはメッセージングフックプロバイダーがメッセージの再ルーティング中にメッセージを削除した可能性があるかどうかを示します。
  
クライアントアプリケーションでこのプロパティを設定することはできません。 受信メッセージの場合、クライアントまたはサービスプロバイダーは、このプロパティに[imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して、メッセージの状態を確認できます。 値 S_OK は、メッセージがメッセージストアに正常に配信されたことを示します。 値 MAPI_E_OBJECT_DELETED は、メッセージが削除され、ストアにコミットされていないことを示します。 
  
メッセージストアプロバイダーは、メッセージ、受信者テーブル、および送信キューテーブルでこのプロパティをサポートしている必要があります。 クライアントとプロバイダーは、送信キューテーブルの列を設定し、このプロパティに基づいて制限できる必要があります。
  
## <a name="related-resources"></a>関連リソース

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

