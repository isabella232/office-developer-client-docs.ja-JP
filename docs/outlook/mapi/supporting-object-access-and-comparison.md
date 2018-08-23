---
title: オブジェクトのアクセスと比較のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f33dcedae5ffe30b85a58d5248d239be81c8efc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575282"
---
# <a name="supporting-object-access-and-comparison"></a>オブジェクトのアクセスと比較のサポート

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サービス プロバイダーでは、開くし、プロバイダーやその他のプロバイダーに属しているオブジェクトを比較する、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドと[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)メソッドを使用できます。 
  
クライアントの[IMAPISession::OpenEntry](imapisession-openentry.md)をのようなプロバイダーは、オブジェクトのエントリ id を知っている、長い間の任意のオブジェクトにアクセスするためのサポート オブジェクトの**OpenEntry**メソッドを使用できます。 サポート メソッドでは、セッション メソッドとは異なり、 _lpEntryID_パラメーターに有効なエントリの識別子を指定することが必要です。 NULL にすることはできません。 
  
トランスポート プロバイダーが**IMAPISupport::OpenEntry**を使用する方法を示すためには、次のシナリオを検討します。 トランスポート プロバイダーは、リッチ テキスト形式で書式設定されたメッセージを受信しましたが、対象の受信者がこの形式を処理できるかどうかがわからない メッセージを配信する前にトランスポート プロバイダーは、次の操作を必要があります。
  
1. 受信者と受信者のエントリの識別子、その**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティにアクセスするためのメッセージの[IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出します。
    
2. 開くには、受信者は、通常、 **IMAPISupport::OpenEntry**にメッセージのユーザーまたは配布リストに対応するエントリの識別子を渡します。 プロバイダーできませんを事前に確認、受信者のオブジェクト タイプであるために、 _lpInterface_パラメーターを NULL に設定する必要があります。 サポート オブジェクトの**OpenEntry**メソッドでは、受信者のアドレス帳プロバイダーを確認するのには[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出します。 セッション オブジェクト、メソッドを呼び出して適切なアドレス帳プロバイダーの**OpenEntry**受信者を開き、トランスポート プロバイダーへのインターフェイス ポインターを返します。 
    
3. **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを取得するために、受信者の[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 **PR_SEND_RICH_INFO**を TRUE に設定すると、受信者が書式設定されたテキストを処理できます。 
    
他のプロバイダーから複数のオブジェクトを開いた場合は、2 つのエントリ id が同じオブジェクトを参照するかどうかを確認する必要があります。 などの短期的なエントリ id がある場合があり、長期のエントリ id とこれらの識別子は、同じオブジェクトを識別しない場合があります。 冗長な処理を避けるためには、これらのエントリ id を比較する[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)メソッドを呼び出します。 エントリ id を直接比較できないためには、エントリの識別子の比較のためこのメソッドを使用する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

