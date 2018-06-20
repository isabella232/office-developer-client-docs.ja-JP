---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9da9a13f87eac097fba078da1f1d6c3f78f69c0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801014"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**適用されます**: Outlook 
  
メッセージ ストア プロバイダーは、送信されたメッセージの処理を実行できるようにします。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]処理されるメッセージのエントリの識別子へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 送信済みメッセージの処理が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージ ストア プロバイダーは、送信済みメッセージの処理をサポートしていません。 呼び出し元は、MAPI スプーラーではない場合、エラー値が返されます。
    
## <a name="remarks"></a>備考

**IMsgStore::FinishedMsg**メソッドでは、送信されたメッセージの処理を実行します。 この処理には、別のフォルダー、または両方のアクションに移動すること、メッセージの削除が含まれます。 処理の種類は、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) と**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定するかどうかによって異なります。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

実装では、 **FinishedMsg**の_lpEntryID_で識別されるメッセージのロックを解除し、適切な処理を実行します。 移行先のメッセージは常にロックされます。MAPI スプーラーは、決して**FinishedMsg**にロックされていないメッセージのエントリ id を渡します。
  
**PR_DELETE_AFTER_SUBMIT**または**PR_SENTMAIL_ENTRYID**が設定されて、両方を設定するでもどちらか一方を設定します。 次の表には、設定に基づいて取るべきアクションについて説明します。 
  
|||
|:-----|:-----|
|場合は 2 つのプロパティを設定します。  <br/> |(通常、[送信トレイ]) の送信、元のフォルダーにメッセージを残します。  <br/> |
|両方のプロパティが設定されます。 場合、  <br/> |必要な場合にメッセージを指定されたフォルダーに移動し、そのパーティションを削除します。  <br/> |
|場合は PR_SENTMAIL_ENTRYID が設定されます。  <br/> |指定されたフォルダーにメッセージを移動します。  <br/> |
|場合は PR_DELETE_AFTER_SUBMIT が設定されます。  <br/> |メッセージを削除します。  <br/> |
   
適切な処理を実行した後は、 [IMAPISupport::DoSentMail](imapisupport-dosentmail.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

