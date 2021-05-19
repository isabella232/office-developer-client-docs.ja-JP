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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427088"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーが送信されたメッセージに対して処理を実行できます。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]処理するメッセージのエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 送信されたメッセージの処理が成功しました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージ ストア プロバイダーは、送信されたメッセージ処理をサポートしていない。 呼び出し元が MAPI スプーラーではない場合、このエラー値が返されます。
    
## <a name="remarks"></a>注釈

**IMsgStore::FinishedMsg** メソッドは、送信されたメッセージに対して処理を実行します。 この処理には、メッセージの削除、別のフォルダーへの移動、または両方のアクションが含まれる場合があります。 処理の種類は **、PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティと **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティが設定されるかどうかによって異なります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**FinishedMsg の実装で**_、lpEntryID_ によって識別されるメッセージのロックを解除し、適切な処理を実行します。 ターゲット メッセージは常にロックされます。MAPI スプーラーは、ロックされていないメッセージのエントリ識別子を **FinishedMsg に渡す必要があります**。
  
設定されているファイルまたは **PR_DELETE_AFTER_SUBMIT、PR_SENTMAIL_ENTRYID** 設定、または設定されている場合があります。 次の表では、設定に基づいて実行する必要があるアクションについて説明します。 
  
|||
|:-----|:-----|
|どちらのプロパティも設定しない場合:  <br/> |メッセージは、送信されたフォルダー (通常は送信箱) に残します。  <br/> |
|両方のプロパティが設定されている場合:  <br/> |必要に応じて、メッセージを指定したフォルダーに移動し、削除します。  <br/> |
|このPR_SENTMAIL_ENTRYID設定されている場合は、次の値を使用します。  <br/> |メッセージを指定したフォルダーに移動します。  <br/> |
|このPR_DELETE_AFTER_SUBMIT設定されている場合は、次の値を使用します。  <br/> |メッセージを削除する。  <br/> |
   
適切な操作を実行した後 [、IMAPISupport::D oSentMail メソッドを呼び出](imapisupport-dosentmail.md) します。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

