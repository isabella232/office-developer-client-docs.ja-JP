---
title: PidTagSentRepresentingSmtpAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d3a3545c544c7b5cf5200468a94edf720dd326e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803529"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a>PidTagSentRepresentingSmtpAddress 標準プロパティ

  
  
**適用対象**: Outlook 
  
送信者はメッセージのユーザーの簡易メール転送プロトコル (SMTP) 電子メール アドレスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SENT_REPRESENTING_SMTP_ADDRESS、PR_SENT_REPRESENTING_SMTP_ADDRESS_A、PR_SENT_REPRESENTING_SMTP_ADDRESS_W  <br/> |
|識別子:  <br/> |0x5D02  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージに送信者によって表されるユーザーのアドレスのプロパティの例です。 クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。 通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。
  
トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。 設定しない場合は、トランスポート プロバイダーは、必要がありますプロパティを設定する**PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md))、メッセージの送信のコピーとローカル コピーに設定されていないまま。
  
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
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
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

