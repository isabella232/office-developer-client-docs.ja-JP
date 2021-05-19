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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418786"
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

 _ulUIParam_
  
> [in]フォームを開いている間に表示される進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。 
    
 _ulFlags_
  
> [in]フォームの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> ユーザー インターフェイスを表示して、状態を提供するか、ユーザーに詳細を求めるプロンプトを表示します。 このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラスの文字列のみを解決する必要があります。
    
 _lpszMessageClass_
  
> [in]読み込むメッセージのメッセージ クラスを示す文字列へのポインター。 _lpszMessageClass_ パラメーターで NULL が渡された場合、メッセージ クラスは _pmsg_ パラメーターが指すメッセージから決定されます。 
    
 _ulMessageStatus_
  
> [in]メッセージの状態に関する情報を提供するメッセージの **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたクライアント定義フラグまたはプロバイダー定義フラグのビットマスク。 _lpszMessageClass_ が NULL 以外の場合は _、ulMessageStatus_ パラメーターを設定する必要があります。それ以外の場合 _、ulMessageStatus は_ 無視されます。 
    
 _ulMessageFlags_
  
> [in]メッセージの現在の状態を示す **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。 _lpszMessageClass が_ NULL 以外の場合は _、ulMessageFlags_ パラメーターを設定する必要があります。それ以外の場合 _、ulMessageFlags は_ 無視されます。 
    
 _pFolderFocus_
  
> [in]メッセージを直接含むフォルダーへのポインター。 _pFolderFocus_ パラメーターは、そのようなフォルダーが存在しない場合は NULL にできます (たとえば、メッセージが別のメッセージに埋め込まれている場合)。 
    
 _pMessageSite_
  
> [in]メッセージのメッセージ サイトへのポインター。
    
 _pmsg_
  
> [in]メッセージへのポインター。
    
 _pViewContext_
  
> [in]メッセージのビュー コンテキストへのポインター。 _pViewContext パラメーター_ には NULL を指定できます。 
    
 _riid_
  
> [in]返されるフォーム オブジェクトに使用するインターフェイスのインターフェイス識別子 (IID)。 _riid パラメーターは_ NULL にすることはできません。 
    
 _ppvObj_
  
> [out]返されたインターフェイスへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> フォームは、要求されたインターフェイスをサポートしていない。
    
MAPI_E_NOT_FOUND 
  
> _lpszMessageClass_ で渡されたメッセージ クラスは、フォーム ライブラリ内のフォームのメッセージ クラスと一致しません。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::LoadForm** メソッドを呼び出して、既存のメッセージのフォームを開きます。 **LoadForm** はフォーム オブジェクトを開き、メッセージをフォーム オブジェクトに読み込み、必要に応じて適切なビュー コンテキストを設定し、フォーム オブジェクトの要求されたインターフェイスを返します。 
  
_pFolderFocus パラメーター_ は、メッセージを含むフォルダーをポイントします。 メッセージが別のメッセージに埋め込まれている場合  _、pFolderFocus は_ NULL である必要があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lpszMessageClass_ で NULL が渡された場合、実装はメッセージの PR_MESSAGE_CLASS [(PidTagMessageClass)、PR_MSG_STATUS](pidtagmessageclass-canonical-property.md)プロパティ、および PR_MESSAGE_FLAGS プロパティからメッセージのメッセージ クラス、状態、**フラグを取得** します。  _lpszMessageClass_ にメッセージ クラス文字列が指定されている場合、実装では _ulMessageStatus_ および _ulMessageFlags の値を使用する必要があります_。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI では **、IMAPIFormMgr::LoadForm** メソッドを使用してフォームを読み込み、表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[PidTagMessageClass 標準プロパティ](pidtagmessageclass-canonical-property.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

