---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419850"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを開きます。
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番フォームが開かれている間に表示される進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで MAPI_DIALOG フラグが設定されていない場合は無視されます。 
    
 _ulFlags_
  
> 順番フォームを開く方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 状態を提供するユーザーインターフェイスを表示します。詳細については、ユーザーに確認します。 このフラグが設定されていない場合、ユーザーインターフェイスは表示されません。
    
 _pfrminfoToActivate_
  
> 順番フォームを開くために使用されるフォーム情報オブジェクトへのポインター。
    
 _refiidtoask_
  
> 順番作成された form オブジェクトに対して返されるインターフェイスのインターフェイス識別子 (IID) へのポインター。 _refiidtoask_パラメーターを NULL にすることはできません。 
    
 _ppvObj_
  
> 読み上げ返されるインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> 要求されたインターフェイスは、form オブジェクトでサポートされていません。
    
## <a name="remarks"></a>注釈

フォーム閲覧者は、 **imapiformmgr:: CreateForm**メソッドを呼び出して、フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを開きます。 指定したフォーム情報オブジェクトで説明されているフォームのフォームサーバーのインスタンスを作成することによって、 **CreateForm**によってフォームが開きます。 必要に応じて、 **CreateForm**は[imapiformmgr::P repareform](imapiformmgr-prepareform.md)メソッドを呼び出して、フォームサーバーコードをユーザーのディスクにダウンロードします。 
  
_pfrminfoToActivate_パラメーターは、正しく解決されたフォーム情報オブジェクトを指している必要があります。 
  
フォームを開いた後、呼び出し元フォームビューアーでは、 [IPersistMessage](ipersistmessageiunknown.md)インターフェイスを使用してメッセージを設定し、必要に応じてフォームのビューコンテキストを設定できます。 詳細については、「[フォームサーバーの起動](launching-a-form-server.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |createanddisplaynewmailinfolder  <br/> |mfcmapi は、 **imapiformmgr:: CreateForm**メソッドを使用して、表示する前にフォームを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[フォームサーバーの起動](launching-a-form-server.md)

