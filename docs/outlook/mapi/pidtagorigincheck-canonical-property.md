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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435762"
---
# <a name="pidtagorigincheck-canonical-property"></a>PidTagOriginCheck 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配信レポートの受信者が元のメッセージの送信元を確認できるようにするバイナリ検証値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGIN_CHECK  <br/> |
|識別子:  <br/> |0x0027  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、送信されたメッセージの送信元を確認するために、メッセージ転送エージェント (MTA)、または配信レポートを受信するメッセージングユーザーなどのサードパーティに対して、手段を提供します。 受信したメッセージにこのプロパティがある場合は、メッセージへの応答として生成された配信レポートにこのプロパティをコピーする必要があります。
  
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

