---
title: PidTagReceivedRepresentingEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 12e4c97947cfe579f550cc6d48ca0b64750b9ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803260"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a>PidTagReceivedRepresentingEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
受信側ユーザーはメッセージング ユーザーのエントリの識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RCVD_REPRESENTING_ENTRYID  <br/> |
|識別子:  <br/> |0x0043  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
