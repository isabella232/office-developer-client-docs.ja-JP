---
title: PidLidValidFlagStringProof 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315387"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>PidLidValidFlagStringProof 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) プロパティの値が **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) プロパティの値を知っているエージェントによって設定されたかどうかを検証します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidValidFlagStringProof  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085BF  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

送信不可オブジェクト (受信メールオブジェクトとメール以外のオブジェクト) では、クライアントは **dispidRequest** を変更するときに、この値を PR_MESSAGE_DELIVERY_TIME に設定する必要があります。 
  
**PR_MESSAGE_DELIVERY_TIME** の値は送信者によって予測できないので、このプロパティの値が **PR_MESSAGE_DELIVERY_TIME** の値と等しい場合 **、dispidRequest** の値がメッセージの送信者から発生しなかったのは合理的に確実です。 クライアントは、クライアントの特定のセキュリティ ポリシーに従って、この比較の結果に基づいて **、dispidRequest** の値をエンド ユーザーに提示する方法を決定できます。 **dispidFlagStringEnum** ([PidLidFlagString)](pidlidflagstring-canonical-property.md)の値が存在するために **dispidRequest** の値が無視される場合は、このプロパティを無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidTagMessageDeliveryTime 標準プロパティ](pidtagmessagedeliverytime-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

