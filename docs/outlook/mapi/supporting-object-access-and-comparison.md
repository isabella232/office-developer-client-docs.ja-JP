---
title: サポート オブジェクトのアクセスと比較
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
# <a name="supporting-object-access-and-comparison"></a>サポート オブジェクトのアクセスと比較

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーは [、IMAPISupport::OpenEntry](imapisupport-openentry.md) メソッドと [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) メソッドを使用して、プロバイダーまたは他のプロバイダーに属するオブジェクトを開いて比較できます。 
  
[クライアントの IMAPISession::OpenEntry](imapisession-openentry.md)と同様に、プロバイダーはサポート オブジェクトの **OpenEntry** メソッドを使用して、オブジェクトのエントリ識別子を知っている限り、任意のオブジェクトにアクセスできます。 セッション メソッドとは異なり、サポート メソッドでは  _、lpEntryID_ パラメーターに有効なエントリ識別子を指定する必要があります。 NULL にすることはできません。 
  
トランスポート プロバイダーが **IMAPISupport::OpenEntry** を使用する方法を説明するには、次のシナリオを検討してください。 トランスポート プロバイダーはリッチ テキスト形式で書式設定されたメッセージを受信し、ターゲット受信者がこの形式を処理できるかどうかを知りません。 メッセージを配信する前に、トランスポート プロバイダーは次の操作を行う必要があります。
  
1. **メッセージ** の [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出して、受信者テーブルと受信者のエントリ識別子 、その PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティにアクセスします。
    
2. エントリ識別子を **IMAPISupport::OpenEntry** に渡して、受信者 (通常はメッセージング ユーザーまたは配布リスト) を開きます。 プロバイダーが受信者のオブジェクトの種類を前もって知らないので  _、lpInterface_ パラメーターを NULL に設定する必要があります。 サポート オブジェクトの **OpenEntry** メソッドは [IMAPISession::OpenEntry](imapisession-openentry.md) を呼び出して、受信者を担当するアドレス帳プロバイダーを決定します。 セッション オブジェクトは、適切なアドレス帳プロバイダーの **OpenEntry** メソッドを呼び出して、受信者を開き、トランスポート プロバイダーへのインターフェイス ポインターを返します。 
    
3. 受信者の [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを取得します。 この **PR_SEND_RICH_INFO** TRUE に設定されている場合、受信者は書式設定されたテキストを処理できます。 
    
他のプロバイダーから複数のオブジェクトを開いている場合は、2 つのエントリ識別子が同じオブジェクトを参照するかどうかを確認する必要があります。 たとえば、短期エントリ識別子と長期エントリ識別子を持つ場合、これらの識別子は同じオブジェクトを識別する場合と識別できない場合があります。 冗長処理を回避するには [、IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) メソッドを呼び出して、これらのエントリ識別子を比較します。 エントリ識別子を直接比較できないので、エントリ識別子の比較にはこのメソッドを使用する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

