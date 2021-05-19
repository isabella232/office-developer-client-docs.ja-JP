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
  
フォームを開き、フォームのメッセージ クラスに基づいて新しいメッセージを作成します。
  
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

 _ulUIParam_
  
> [in]フォームを開いている間に表示される進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _ulFlags_
  
> [in]フォームの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> ユーザー インターフェイスを表示して、状態を提供するか、ユーザーに詳細を求めるプロンプトを表示します。 このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。
    
 _pfrminfoToActivate_
  
> [in]フォームを開くのに使用されるフォーム情報オブジェクトへのポインター。
    
 _refiidToAsk_
  
> [in]作成されたフォーム オブジェクトに対して返されるインターフェイスのインターフェイス識別子 (IID) へのポインター。 _refiidToAsk_ パラメーターは NULL にすることはできません。 
    
 _ppvObj_
  
> [out]返されたインターフェイスへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> 要求されたインターフェイスは、フォーム オブジェクトではサポートされていません。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::CreateForm** メソッドを呼び出してフォームを開き、フォームのメッセージ クラスに基づいて新しいメッセージを作成します。 **CreateForm** は、指定されたフォーム情報オブジェクトで説明したように、そのフォームのフォーム サーバーのインスタンスを作成してフォームを開きます。 必要に応じて **、CreateForm** は [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) メソッドを呼び出して、フォーム サーバー コードをユーザーのディスクにダウンロードします。 
  
_pfrminfoToActivate_ パラメーターは、正しく解決されたフォーム情報オブジェクトを指している必要があります。 
  
フォームを開いた後、呼び出し元のフォーム ビューアーは [、IPersistMessage](ipersistmessageiunknown.md) インターフェイスを使用してメッセージを設定する必要があります。必要に応じて、フォームのビュー コンテキストを設定できます。 詳細については、「フォーム サーバーの [起動」を参照してください](launching-a-form-server.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI は **、IMAPIFormMgr::CreateForm** メソッドを使用して、フォームを表示する前にフォームを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[フォーム サーバーの起動](launching-a-form-server.md)

