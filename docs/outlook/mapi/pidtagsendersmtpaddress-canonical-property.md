---
title: PidTagSenderSmtpAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342631"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a>PidTagSenderSmtpAddress 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メールボックス所有者の簡易メール トランスポート プロトコル (SMTP) 電子メール アドレスの形式が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SENDER_SMTP_ADDRESS、PR_SENDER_SMTP_ADDRESS_A、PR_SENDER_SMTP_ADDRESS_W  <br/> |
|識別子:  <br/> |0x5D01  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ送信者のアドレス プロパティの例です。 これは、送信トランスポート プロバイダーによって設定する必要があります。これは、以前に既存の値を伝達する必要があります。
  
送信側アドレスプロパティを提供しているトランスポート プロバイダーがない場合、MAPI スプーラーは、エントリ識別子の [IMAPISession::QueryIdentity](imapisession-queryidentity.md) メソッドを呼び出して、それらを入力します。 エントリ識別子が指定されていない場合は、MAPI スプーラーは、種類が PT_UNICODE または PT_STRING8 のすべての送信者アドレス プロパティに "不明" を格納します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのMicrosoft Exchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> ポスト オブジェクトに対して許容されるプロパティと操作を指定します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> 連絡先および個人用配布リスト オブジェクトに対して許容されるプロパティと操作を指定します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

