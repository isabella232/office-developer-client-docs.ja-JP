---
title: PidTagReceivedRepresentingEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 490025f22cd643ffededd6d8022907761c7f15d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567098"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a>PidTagReceivedRepresentingEntryId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
受信側ユーザーはメッセージング ユーザーのエントリの識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RCVD_REPRESENTING_ENTRYID  <br/> |
|識別子:  <br/> |0x0043  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、受信側のユーザーによって表現されているメッセージング ユーザーのアドレスのプロパティのいずれかです。 承認または代理人の確認を担当するも、受信トランスポート プロバイダーによって設定しなければなりません。 表されるは、メッセージング ユーザーがない場合、このプロパティは**PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) のプロパティに含まれているエントリの識別子を設定する必要があります。
  
クライアント アプリケーションに返信する他のクライアントの代理として受信したメッセージ、受信したメッセージからの応答を**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) のプロパティにこのプロパティする必要がありますコピーします。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。
    
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

