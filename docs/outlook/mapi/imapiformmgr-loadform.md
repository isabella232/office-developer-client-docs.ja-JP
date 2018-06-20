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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1f3a876269868c30df48e0a0b62036cfdc199955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800549"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**適用されます**: Outlook 
  
フォームを開くには既存のメッセージを開始します。
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in]フォームを開いたときに表示される進行状況のインジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。 
    
 _ulFlags_
  
> [in]フォームを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> ステータスを指定するか、詳細についてはユーザーの入力を求めるのためのユーザー インターフェイスを表示します。 このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラス文字列のみを解決する必要があります。
    
 _lpszMessageClass_
  
> [in]読み込まれるメッセージのメッセージ クラスの名前を示す文字列へのポインター。 _LpszMessageClass_パラメーターに NULL を渡した場合、メッセージ クラスは、 _pmsg_パラメーターで指定されたメッセージから判断されます。 
    
 _ulMessageStatus_
  
> [in]メッセージの状態に関する情報を提供するメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたクライアント定義またはプロバイダー定義のフラグのビットマスクです。 _LpszMessageClass_は、NULL 以外の場合、 _ulMessageStatus_パラメーターを設定する必要があります。それ以外の場合、 _ulMessageStatus_は無視されます。 
    
 _ulMessageFlags_
  
> [in]フラグは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティ、メッセージの現在の状態を示すメッセージのコピーのビットマップへのポインター。 _LpszMessageClass_は、NULL 以外の場合、 _ulMessageFlags_パラメーターを設定する必要があります。それ以外の場合、 _ulMessageFlags_は無視されます。 
    
 _pFolderFocus_
  
> [in]直接メッセージを含むフォルダーへのポインター。 _PFolderFocus_パラメーターは、(たとえば、メッセージは、別のメッセージに埋め込まれている) 場合、このようなフォルダーが存在しない場合、NULL にすることができます。 
    
 _pMessageSite_
  
> [in]メッセージのメッセージのサイトへのポインター。
    
 _pmsg_
  
> [in]メッセージへのポインター。
    
 _pViewContext_
  
> [in]メッセージのビュー コンテキストへのポインター。 _PViewContext_パラメーターは NULL にできます。 
    
 _riid_
  
> [in]返信されたフォーム オブジェクトに使用するインターフェイスのインターフェイス id (IID)。 _Riid_パラメーターを NULL にする必要がありますはできません。 
    
 _ppvObj_
  
> [out]返されたインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> フォームは、要求されたインターフェイスをサポートしていません。
    
MAPI_E_NOT_FOUND 
  
> _LpszMessageClass_に渡されるメッセージ クラスでは、フォーム ライブラリ内の任意のフォームのメッセージ クラスが一致しません。 
    
## <a name="remarks"></a>備考

フォームの閲覧者は、既存のメッセージのフォームを開くに**IMAPIFormMgr::LoadForm**メソッドを呼び出します。 **LoadForm**フォーム オブジェクトを開きます、フォーム オブジェクトにメッセージを読み込みます、必要に応じて、適切なビューのコンテキストを設定し、フォーム オブジェクトの要求されたインターフェイスを返します。 
  
_PFolderFocus_パラメーターは、メッセージを含むフォルダーを指します。 メッセージは、別のメッセージに埋め込まれている場合_pFolderFocus_は NULL である必要があります。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

実装がメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))、 **PR_MSG_STATUS** **PR_MESSAGE_FLAGS から、メッセージのメッセージ クラス、状態、およびフラグを取得する場合は_lpszMessageClass_に NULL が渡されると、** プロパティ。 _LpszMessageClass_のメッセージ クラスの文字列を指定すると、実装は_ulMessageStatus_と_ulMessageFlags_の値を使用する必要があります。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI では、 **IMAPIFormMgr::LoadForm**メソッドを使用して、表示する前にフォームをロードします。  <br/> |
   
## <a name="see-also"></a>関連項目



[PidTagMessageClass の標準的なプロパティ](pidtagmessageclass-canonical-property.md)
  
[PidTagMessageFlags の標準的なプロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus の標準的なプロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

