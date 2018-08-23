---
title: PidTagSenderEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8efceed4910d057d6dcca742dfe9b8f0010c968e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578676"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a>PidTagSenderEmailAddress 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ送信者の電子メール アドレスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SENDER_EMAIL_ADDRESS、PR_SENDER_EMAIL_ADDRESS_A、PR_SENDER_EMAIL_ADDRESS_W  <br/> |
|識別子:  <br/> |0x0C1F  <br/> |
|データの種類 :   <br/> |PT_UNICOIDE、PT_STRING8  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、メッセージの送信者のアドレスのプロパティの例を示します。 以前の既存の値を反映する必要があることはありませんが、送信トランスポート プロバイダーによって設定されなければなりません。
  
トランスポート プロバイダーは、任意の送信者アドレスのプロパティを指定しない場合、MAPI スプーラーはメソッドを呼び出して、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)のエントリ id を入力しようとします。 エントリ id が指定されていません、MAPI スプーラーは PT_TSTRING の種類のすべての送信者アドレスのプロパティで「不明」を格納します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> 投稿オブジェクトのプロパティとは、許可の操作を指定します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。
    
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

