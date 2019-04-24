---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321696"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存のメッセージを開くフォームを開始します。
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
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
    
MAPIFORM_EXACTMATCH 
  
> 完全一致のメッセージクラス文字列のみを解決する必要があります。
    
 _lpszmessageclass_
  
> 順番読み込むメッセージのメッセージクラスの名前を示す文字列へのポインター。 NULL が_lpszmessageclass_パラメーターで渡された場合、メッセージクラスは_pmsg_パラメーターによって示されるメッセージから判断されます。 
    
 _ulmessagestatus_
  
> 順番メッセージの状態に関する情報を提供する、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされた、クライアント定義またはプロバイダー定義のフラグのビットマスク。 _lpszmessageclass_が NULL 以外の場合は_ulmessagestatus_パラメーターを設定する必要があります。それ以外の場合、 _ulmessagestatus_は無視されます。 
    
 _ulmessageflags_
  
> 順番メッセージの現在の状態を示す、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。 _lpszmessageclass_が NULL 以外の場合は、 _ulmessageflags_パラメーターを設定する必要があります。それ以外の場合、 _ulmessageflags_は無視されます。 
    
 _pfolderfocus_
  
> 順番直接メッセージを含むフォルダーへのポインター。 このようなフォルダーが存在しない場合 (たとえば、メッセージが別のメッセージに埋め込まれている場合) は、 _pfolderfocus_パラメーターを NULL にすることができます。 
    
 _pメッセージ ite_
  
> 順番メッセージのメッセージサイトへのポインター。
    
 _pmsg_
  
> 順番メッセージへのポインター。
    
 _pviewcontext_
  
> 順番メッセージのビューコンテキストへのポインター。 _pviewcontext_パラメーターは NULL にすることができます。 
    
 _riid_
  
> 順番返される form オブジェクトに対して使用されるインターフェイスのインターフェイス識別子 (IID)。 _riid_パラメーターを NULL にすることはできません。 
    
 _ppvObj_
  
> 読み上げ返されるインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> フォームでは、要求されたインターフェイスがサポートされていません。
    
MAPI_E_NOT_FOUND 
  
> _lpszmessageclass_で渡されるメッセージクラスが、フォームライブラリ内のフォームのメッセージクラスと一致しません。 
    
## <a name="remarks"></a>解説

フォーム閲覧者は、 **imapiformmgr:: loadform**メソッドを呼び出して、既存のメッセージのフォームを開きます。 **loadform**は form オブジェクトを開き、form オブジェクトにメッセージを読み込み、必要に応じて適切なビューコンテキストを設定し、form オブジェクトの要求されたインターフェイスを返します。 
  
_pfolderfocus_パラメーターは、メッセージを含むフォルダーを指します。 メッセージが別のメッセージに埋め込まれている場合、 _pfolderfocus_は NULL である必要があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lpszmessageclass_で NULL が渡されると、メッセージのメッセージクラス、状態、およびフラグがメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))、 **PR_MSG_STATUS** 、および PR_MESSAGE_FLAGS から取得されます。 **** プロパティ。 メッセージクラスの文字列が_lpszmessageclass_で提供されている場合、この実装では_ulmessagestatus_および_ulmessagestatus_の値を使用する必要があります。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |openmessagenonmodal  <br/> |mfcmapi は、 **imapiformmgr:: loadform**メソッドを使用して、表示する前にフォームを読み込みます。  <br/> |
   
## <a name="see-also"></a>関連項目



[PidTagMessageClass 標準プロパティ](pidtagmessageclass-canonical-property.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

