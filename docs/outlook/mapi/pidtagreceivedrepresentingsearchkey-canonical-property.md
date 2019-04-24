---
title: PidTagReceivedRepresentingSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bcf310138e4b43b1cc36a177194f721c401caba6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356820"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a>PidTagReceivedRepresentingSearchKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信側ユーザーによって表されるメッセージングユーザーの検索キーが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RCVD_REPRESENTING_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x0052  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、受信側ユーザーによって表されるメッセージングユーザーのアドレスプロパティの1つです。 これは、受信トランスポートプロバイダーによって設定される必要があります。これは、代理人の承認または検証も行います。 メッセージングユーザーが表示されていない場合、このプロパティは**PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) プロパティに含まれる検索キーに設定する必要があります。
  
他のクライアントに代わって受信したメッセージに応答するクライアントアプリケーションは、受信したメッセージから、返信の**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) プロパティにこのプロパティをコピーする必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序と流れを処理します。
    
[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。
    
[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。
    
[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[PidTagSearchKey 標準プロパティ](pidtagsearchkey-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

