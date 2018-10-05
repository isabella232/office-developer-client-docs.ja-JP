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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391956"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>PidLidValidFlagStringProof 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**DispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) プロパティの値は**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) プロパティの値を知っているエージェントによって設定されたかどうかを検証します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidValidFlagStringProof  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085BF  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

非うっかり (受信したメールやメール以外のオブジェクト)、オブジェクトの**dispidRequest**を変更する場合、クライアントは必要があります**PR_MESSAGE_DELIVERY_TIME**の値にこの値を設定します。
  
**PR_MESSAGE_DELIVERY_TIME**の値は、このプロパティの値が**PR_MESSAGE_DELIVERY_TIME**の値と等しい場合に、送信者が予測できない、ため、確信が**dispidRequest**の値がありませんでした。メッセージの送信者から発信します。 クライアントは、クライアントの特定のセキュリティ ポリシーに従ってこの比較の結果に基づいてユーザーに**dispidRequest**の値を表示する方法を決定できます。 **DispidRequest**の値は無視する場合は**dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) の値が存在するので、このプロパティは無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidTagMessageDeliveryTime 標準プロパティ](pidtagmessagedeliverytime-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

