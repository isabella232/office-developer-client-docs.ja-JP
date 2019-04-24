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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315387"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>PidLidValidFlagStringProof 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) プロパティの値を知っているエージェントによって、 **dispidrequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) プロパティの値が設定されているかどうかを検証します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidvalidflagstringproof  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x000085bf  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

送信可能以外のオブジェクト (受信メールオブジェクトとメール以外のオブジェクト) では、 **dispidrequest**を変更するときに、クライアントはこの値を**PR_MESSAGE_DELIVERY_TIME**の値に設定する必要があります。
  
**PR_MESSAGE_DELIVERY_TIME**の値を送信者が予測することはできないため、このプロパティの値が**PR_MESSAGE_DELIVERY_TIME**の値と等しい場合、 **dispidrequest**の値が次の値でないことが合理的であることを示します。メッセージの送信者から発信されます。 クライアントは、クライアントの特定のセキュリティポリシーに従って、この比較の結果に基づいて、 **dispidrequest**の値をエンドユーザーに提示する方法を決定することができます。 **dispidflagstringenum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) の値が存在するために**dispidrequest**の値が無視される場合、このプロパティは無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidTagMessageDeliveryTime 標準プロパティ](pidtagmessagedeliverytime-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

