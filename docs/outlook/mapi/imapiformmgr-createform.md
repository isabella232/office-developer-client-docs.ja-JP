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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e86c3d9678739c09024c0655cbbbb702749a53f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586166"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームのメッセージ クラスに基づく新しいメッセージを作成するフォームを開きます。
  
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
  
> [in]フォームを開いたときに表示される進行状況のインジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。 
    
 _ulFlags_
  
> [in]フォームを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> ステータスを指定するか、詳細についてはユーザーの入力を求めるのためのユーザー インターフェイスを表示します。 このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。
    
 _pfrminfoToActivate_
  
> [in]フォームを開くために使用されるフォームの情報オブジェクトへのポインター。
    
 _refiidToAsk_
  
> [in]作成されたフォーム オブジェクトを取得するインターフェイスのインターフェイス id (IID) へのポインター。 _RefiidToAsk_パラメーターを NULL にする必要がありますはできません。 
    
 _ppvObj_
  
> [out]返されたインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> フォーム オブジェクトでは、要求されたインターフェイスはサポートされていません。
    
## <a name="remarks"></a>注釈

フォームの閲覧者は、フォームのメッセージ クラスに基づく新しいメッセージを作成するフォームを開くに**IMAPIFormMgr::CreateForm**メソッドを呼び出します。 **CreateForm**は、情報の指定されたフォーム オブジェクトの説明に従って、そのフォームに対するフォーム サーバーのインスタンスを作成することでフォームを開きます。 必要な場合、 **CreateForm**は、フォームのサーバー コードをユーザーのディスクにダウンロードする[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)メソッドを呼び出します。 
  
_PfrminfoToActivate_パラメーターは、正しく解決されているフォーム情報オブジェクト] をポイントする必要があります。 
  
フォームを開いた後に、呼び出し元のフォーム ビューアーは[IPersistMessage](ipersistmessageiunknown.md)インターフェイスを使用してメッセージを設定する必要があり、フォームのビュー コンテキストを必要に応じて設定できます。 詳細については、[フォームのサーバーを起動する](launching-a-form-server.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI では、 **IMAPIFormMgr::CreateForm**メソッドを使用して、表示する前にフォームを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[フォーム サーバーの起動](launching-a-form-server.md)

