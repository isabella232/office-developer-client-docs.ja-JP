---
title: PidTagOriginCheck 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 27b967b885ef35c04d52699c289dd60248e9abd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581084"
---
# <a name="pidtagorigincheck-canonical-property"></a>PidTagOriginCheck 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
配信レポートの受信者を元のメッセージの発生元を検証するを有効にするバイナリの検証値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGIN_CHECK  <br/> |
|識別子:  <br/> |0x0027  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、送信されたメッセージの送信元を確認するメッセージ転送エージェント (MTA) または配信レポートを受信するメッセージングのユーザーなどのサード パーティ製の手段を提供します。 受信したメッセージに存在する場合、このプロパティは、メッセージへの応答として生成されるすべての配信レポートをコピーしてください。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

