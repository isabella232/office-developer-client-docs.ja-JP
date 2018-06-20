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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e237e73f59fa691821dcb55b59f5d17518451797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801100"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**適用されます**: Outlook 
  
新しいメッセージを初期化します。
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameters

 _pMessageSite_
  
> [in]ビューアーでのメッセージを操作するのには、フォームを使用するメッセージのサイトへのポインター。
    
 _pMessage_
  
> [in]新しいメッセージへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しいメッセージが正常に初期化しました。
    
## <a name="remarks"></a>備考

フォーム ビューアーは、ユーザーがフォームを処理するメッセージ クラスが所属する新しいメッセージを書き込むときに、 **IPersistMessage::InitNew**メソッドを呼び出します。 フォーム オブジェクトに有効なユーザー インターフェイスのポインターがある場合は、メッセージ オブジェクトのユーザー インターフェイスが表示されます。 
  
 **InitNew**呼び出せませんフォームが[初期化されていない](uninitialized-state.md)状態以外の任意の状態にします。 **InitNew**が呼び出されたときに、フォームは他の状態のいずれかでは場合は、E_UNEXPECTED を返します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

通常、プロパティが保存されていないメッセージは変更済みとしてマーク、クライアントがユーザーの入力を求めるダイアログ ボックスを表示できるようにこれらのプロパティを保存するかどうか。 ユーザーは、メッセージを保存する必要があることを示している場合は、データを保存し、クリーンとしてメッセージをマーク、正常終了します。
  
ただし、新たに初期化されたメッセージの処理は、いずれかを設定またはプロパティでは、以上の計算、それらのプロパティを保存する必要をオフにメッセージを変更されたとします。 プロパティがユーザーに表示する必要がありますが計算するためダイアログ ボックスが表示されません。
  
**InitNew**に渡される 1 つは別の作業中のメッセージ、サイトへの参照は、フォームに場合、は、使用できなくするために元のサイトをリリースします。 _PMessageSite_と_pMessage_パラメーターからは、サイトのメッセージとメッセージへのポインターを格納し、その参照カウントをインクリメントするのには、両方のオブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。 
  
メッセージ クラスの適切な**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) と**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))、新しいメッセージのプロパティを設定します。 多くのメッセージ クラスは、新しいメッセージの**PR_MESSAGE_FLAGS**を MSGFLAG_UNSENT などの設定します。 
  
戻る前にフォームにエラーがない場合は、[通常](normal-state.md)状態の遷移が発生しました。 [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出すことによって登録されているすべてのビューアーに新着メッセージの通知を送信して、S_OK を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**InitNew**の呼び出しが成功したら、次の必要なプロパティおよびその他、フォームに設定されていることを引き受けることができます。
  
 **PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
フォームの状態の詳細については、[フォームの状態](form-states.md)を参照してください。 ストレージ ・ オブジェクトを初期化する方法の詳細については、 [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)メソッドを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

