---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591038"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
別のフォルダーに 1 つのフォルダーからのコピーや移動メッセージです。
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpSrcInterface_
  
> [in]コピーまたは移動するメッセージを含むフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcFolder_
  
> [in]コピーまたは移動するメッセージを含むフォルダーへのポインター。
    
 _lpMsgList_
  
> [in]コピーまたは移動するメッセージを識別するエントリの識別子の配列へのポインター。 
    
 _lpDestInterface_
  
> [in]コピーまたは移動されたメッセージのコピー先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpDestFolder_
  
> [in]先のフォルダーにコピーまたは移動されたメッセージへのポインター。 このフォルダーを開く必要があります。
    
 _ulUIParam_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を実現する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MESSAGE_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
MESSAGE_MOVE 
  
> メッセージを移動する必要があるのではなくコピーします。 MESSAGE_MOVE が設定されていない場合、メッセージがコピーされます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> コピーまたは移動操作が正常に完了しました。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::CopyMessages**メソッドを実装します。 メッセージ ストア プロバイダーは、コピーまたは別の 1 つのフォルダーから 1 つまたは複数のメッセージを移動するのには、 [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)の実装では、 **IMAPISupport::CopyMessages**を呼び出すことができます。 **IMAPISupport::CopyMessages**の呼び出しの一部として、メッセージ ストア プロバイダーが、MAPI は、進行状況インジケーターを表示することを指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

