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

 _pメッセージ ite_
  
> 順番フォームがビューアー内のメッセージを操作するために使用するメッセージサイトへのポインター。
    
 _pmessage_
  
> 順番新しいメッセージへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいメッセージが正常に初期化されました。
    
## <a name="remarks"></a>解説

フォームビューアーは、フォームが処理するメッセージクラスに属する新しいメッセージをユーザーが書き込むときに、 **IPersistMessage:: InitNew**メソッドを呼び出します。 form オブジェクトに有効なユーザーインターフェイスポインターがある場合は、そのメッセージオブジェクトのユーザーインターフェイスが表示されます。 
  
 フォームが[初期化](uninitialized-state.md)されていない状態以外の状態にある場合は、 **InitNew**を呼び出すことはできません。 **InitNew**が呼び出されたときに、フォームが他の状態のいずれかになっている場合は、E_UNEXPECTED を返します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

通常、保存されていないプロパティを持つメッセージは変更済みとしてマークされるため、クライアントは、これらのプロパティを保存するかどうかを確認するダイアログボックスを表示することができます。 ユーザーがメッセージを保存することを示している場合は、データを保存し、メッセージを [クリーン] としてマークし、通常どおりに終了します。
  
ただし、新しく初期化されたメッセージを処理する場合は、1つ以上の計算プロパティを設定する必要があります。これらのプロパティを保存する場合は、メッセージを変更済みとしてマークしないようにしてください。 ユーザーは、計算されたプロパティを非表示にする必要があるので、ダイアログボックスを表示する必要はありません。
  
フォームに、 **InitNew**に渡されたものとは異なるアクティブなメッセージサイトへの参照がある場合は、そのサイトが使用されなくなっているため、元のサイトを解放します。 メッセージサイトおよびメッセージへのポインターを pメッセージパラメーター __ と_pmessage_パラメーターから格納し、両方のオブジェクト ' [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して参照カウントをインクリメントします。 
  
新しいメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) および**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティを、自分のメッセージクラスに適したものに設定します。 多くのメッセージクラスでは、たとえば、新しいメッセージの**PR_MESSAGE_FLAGS**を MSGFLAG_UNSENT に設定します。 
  
戻る前に、エラーが発生していない場合は、フォームを[通常](normal-state.md)の状態に移行します。 登録されているすべてのビューアーに新しいメッセージ通知を送信するには、 [IMAPIViewAdviseSink:: onnewmessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出し、S_OK を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**InitNew**を正常に呼び出した後、フォームに対して次の必要なプロパティが設定されていると仮定できます。
  
 **PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
フォームの状態の詳細については、「[フォームの状態](form-states.md)」を参照してください。 ストレージオブジェクトが初期化される方法の詳細については、 [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)メソッドを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

