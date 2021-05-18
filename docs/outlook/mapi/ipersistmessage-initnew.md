---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317151"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージを初期化します。
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>パラメーター

 _pMessageSite_
  
> [in]フォームがビューアーでメッセージを処理するために使用するメッセージ サイトへのポインター。
    
 _pMessage_
  
> [in]新しいメッセージへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいメッセージが正常に初期化されました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは、ユーザーがフォームで処理するメッセージ クラスに属する新しいメッセージを書き込むときに **、IPersistMessage::InitNew** メソッドを呼び出します。 フォーム オブジェクトに有効なユーザー インターフェイス ポインターがある場合は、メッセージ オブジェクトのユーザー インターフェイスが表示されます。 
  
 **InitNew** は、フォームが初期化されていない状態以外の状態にある場合 [は呼び出す必要](uninitialized-state.md) があります。 **InitNew** が呼び出された場合にフォームが他の状態の 1 つにある場合は、次のE_UNEXPECTED。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

通常、保存されていないプロパティを持つメッセージは変更済みとしてマークされ、クライアントは、これらのプロパティを保存するかどうかをユーザーに求めるダイアログ ボックスを表示できます。 ユーザーがメッセージを保存する必要がある場合は、データを保存し、メッセージをクリーンとしてマークし、正常に終了します。
  
ただし、新しく初期化されたメッセージの処理に 1 つ以上の計算プロパティの設定が含まれる場合、それらのプロパティを保存することが重要である場合は、メッセージを変更済みとしてマークしません。 計算されたプロパティはユーザーには表示されない必要があります。ダイアログ ボックスは表示されません。
  
フォームに **InitNew** に渡されるメッセージ サイト以外のアクティブなメッセージ サイトへの参照がある場合は、元のサイトが使用されなくなったため、元のサイトを解放します。 _pMessageSite_ パラメーターと _pMessage_ パラメーターからメッセージ サイトへのポインターとメッセージを格納し、両方のオブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、参照カウントを増やします。 
  
新しいメッセージ **の** PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティと **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティを、メッセージ クラスに適した値に設定します。 たとえば、多くのメッセージ クラスは、新しい **PR_MESSAGE_FLAGS** のMSGFLAG_UNSENTに設定します。 
  
返す前に、エラーが発生したことがない場合は、フォームを [Normal](normal-state.md) 状態に移行します。 [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出して、登録されているすべての閲覧者に新しいメッセージ通知を送信し、S_OK。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**InitNew** を正常に呼び出した後、フォームに対して次の必須プロパティと他のプロパティが設定されていないと仮定できます。
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
フォームの状態の詳細については、「フォームの状態」 [を参照してください](form-states.md)。 記憶域オブジェクトの初期化方法の詳細については [、「IPersistStorage::InitNew メソッド」を参照](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

