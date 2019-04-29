---
title: オブジェクトのアクセスと比較のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429034"
---
# <a name="supporting-object-access-and-comparison"></a>オブジェクトのアクセスと比較のサポート

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーは、 [imapisupport:: openentry](imapisupport-openentry.md)および[imapisupport:: compareentryids](imapisupport-compareentryids.md)メソッドを使用して、そのプロバイダーまたは他のプロバイダーに属するオブジェクトを開いて比較できます。 
  
[imapisession:: openentry](imapisession-openentry.md) for クライアントでは、プロバイダーはサポートオブジェクトの**openentry**メソッドを使用して、オブジェクトのエントリ識別子を知っている限り、任意のオブジェクトにアクセスできます。 session メソッドとは異なり、support メソッドでは、 _lpentryid_パラメーターに有効なエントリ識別子を指定する必要があります。 NULL にすることはできません。 
  
トランスポートプロバイダーが**imapisupport:: openentry**をどのように使用するかを説明するために、次のシナリオを考えてみます。 トランスポートプロバイダーは、リッチテキスト形式で書式設定されたメッセージを受信しましたが、対象の受信者がこの形式を処理できるかどうかを認識しません。 メッセージを配信する前に、トランスポートプロバイダーは次の操作を行う必要があります。
  
1. メッセージの[IMessage:: getrecipient table](imessage-getrecipienttable.md)メソッドを呼び出して、受信者テーブルと受信者のエントリ id ([PidTagEntryId](pidtagentryid-canonical-property.md)) **** プロパティにアクセスします。
    
2. エントリ識別子を**imapisupport:: openentry**に渡して、受信者 (通常はメッセージングユーザーまたは配布リストのいずれか) を開きます。 プロバイダーは受信者のオブジェクトの種類を事前に知ることができないため、 _lpinterface_パラメーターは NULL に設定する必要があります。 サポートオブジェクトの**openentry**メソッドは、受信者のアドレス帳プロバイダーを決定するために[imapisession:: openentry](imapisession-openentry.md)を呼び出します。 その後、session オブジェクトは、適切なアドレス帳プロバイダーの**openentry**メソッドを呼び出して、受信者を開き、トランスポートプロバイダーへのインターフェイスポインターを返します。 
    
3. 受信者の[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、その**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを取得します。 **PR_SEND_RICH_INFO**が TRUE に設定されている場合、受信者は書式付きテキストを処理できます。 
    
他のプロバイダーから複数のオブジェクトを開いている場合は、2つのエントリ識別子が同じオブジェクトを参照しているかどうかを確認する必要があります。 たとえば、短い用語のエントリ id と長期のエントリ識別子がある場合、これらの識別子は同じオブジェクトを識別する場合としない場合があります。 冗長処理を回避するには、これらのエントリ識別子を比較する[imapisupport:: compareentryids](imapisupport-compareentryids.md)メソッドを呼び出します。 エントリ識別子の比較には、このメソッドを使用する必要があります。エントリ識別子は直接比較できません。 
  
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

