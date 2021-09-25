---
title: PidTagSpoolerStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 473f2745a6c3019db4994192fa4b138f1298b6cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591410"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>PidTagSpoolerStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーで使用できる情報に基づいてメッセージの状態を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SPOOLER_STATUS  <br/> |
|識別子:  <br/> |0x0E10  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ オブジェクトの MAPI によって計算されます。
  
このプロパティは受信メッセージにのみ表示され、他のすべての場合に予約されます。 メッセージが最終的な場所に配信されたかどうか、またはメッセージング フック プロバイダーがメッセージを再ルーティング中に削除した可能性があるかどうかを示します。
  
クライアント アプリケーションは、このプロパティを設定する必要があります。 受信メッセージの場合、クライアントまたはサービス プロバイダーは、このプロパティで [IMAPIProp::GetProps](imapiprop-getprops.md) を呼び出して、メッセージの状態を判断できます。 この値S_OKメッセージがメッセージ ストアに正常に配信されたことを示します。 この値MAPI_E_OBJECT_DELETEDメッセージが削除され、ストアにコミットされたことがないことを示します。 
  
メッセージ ストア プロバイダーは、メッセージ、受信者テーブル、および送信キュー テーブルでこのプロパティをサポートする必要があります。 クライアントとプロバイダーは、送信キュー テーブルの列を設定し、このプロパティに基づいて制限できる必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

