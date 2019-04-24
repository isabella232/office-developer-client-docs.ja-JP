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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348763"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーが、送信されたメッセージに対して処理を実行できるようにします。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番処理するメッセージのエントリ id へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 送信済みメッセージの処理に成功しました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージストアプロバイダーは送信メッセージ処理をサポートしていません。 このエラー値は、発信者が MAPI スプーラーではない場合に返されます。
    
## <a name="remarks"></a>解説

**IMsgStore:: FinishedMsg**メソッドは、送信されたメッセージに対して処理を実行します。 この処理には、メッセージの削除、別のフォルダーへの移動、またはその両方の操作が含まれます。 処理の種類は、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) および**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) の各プロパティが設定されているかどうかによって異なります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**FinishedMsg**の実装で、 _l tryid_で識別されたメッセージをロック解除し、適切な処理を実行します。 ターゲットメッセージは常にロックされます。MAPI スプーラーは、ロックされていないメッセージのエントリ識別子を**FinishedMsg**に渡しません。
  
**PR_DELETE_AFTER_SUBMIT**または**PR_SENTMAIL_ENTRYID**のどちらも設定されていないか、どちらかが設定されているか、どちらか一方が設定されている可能性があります。 次の表では、設定に基づいて実行する必要がある処理について説明します。 
  
|||
|:-----|:-----|
|どちらのプロパティも設定されていない場合:  <br/> |メッセージを送信元のフォルダー (通常は送信トレイ) に残します。  <br/> |
|両方のプロパティが設定されている場合:  <br/> |指定したフォルダーにメッセージを移動し、必要に応じて削除します。  <br/> |
|PR_SENTMAIL_ENTRYID が設定されている場合:  <br/> |メッセージを指示されたフォルダーに移動します。  <br/> |
|PR_DELETE_AFTER_SUBMIT が設定されている場合:  <br/> |メッセージを削除します。  <br/> |
   
適切なアクションを実行した後、 [imapisupport::D o送信メール](imapisupport-dosentmail.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

