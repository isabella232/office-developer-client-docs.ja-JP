---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800699"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**適用されます**: Outlook 
  
メッセージ ストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> [in]表示に関連して、共通のアドレス] ダイアログ ボックスおよびその他の親ウィンドウへのハンドル。
    
_cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
_lpEntryID_
  
> [in]メッセージ ・ ストアを開くことのエントリの識別子へのポインター。 _LpEntryID_パラメーターを NULL にする必要がありますはできません。 
    
_lpInterface_
  
> [in]メッセージ ストアへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 メッセージ ストア (**IMsgStore**) の標準的なインターフェイスへのポインターを返すに_lppMDB_パラメーターは、NULL を渡すことです。
    
_ulFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを使用することができます。
    
  - MAPI_BEST_ACCESS: 要求の最大のネットワーク アクセス許可を持つメッセージ ・ ストアを開くことは許可ユーザーと、最大のクライアントのアプリケーションのアクセス許可。 たとえば、クライアントに読み取り/書き込み権限がある場合は、メッセージ ・ ストア開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用のアクセス許可を持つメッセージ ・ ストアを開く必要があります。 
      
  - MAPI_DEFERRED_ERRORS: 正常に完了する**OpenMsgStore**を使用する可能性のあるメッセージの前にストアは、呼び出し側のクライアントに完全に使用可能。 メッセージ ・ ストアを使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。 
      
  - MDB\_NO_DIALOG: ログオン] ダイアログ ボックスが表示されなくなります。 このフラグが設定し、 **OpenMsgStore**が不足している構成については、ユーザーのヘルプを表示しないメッセージ ストアを開くには、MAPI_E_LOGON_FAILED が返されます。 このフラグが設定されていない場合、メッセージ ストア プロバイダーはユーザー名またはパスワードを修正するか、メッセージ ・ ストアへの接続を確立するために必要なその他のアクションを実行するを求めることができます。 
      
  - MDB\_NO_MAIL: メールの送受信のメッセージ ・ ストアを使用いない必要があります。 このフラグを設定すると、MAPI 通知されません、MAPI スプーラーを無効このメッセージ ・ ストアが開かれることです。
      
  - MDB\_オンライン: で Exchange キャッシュ モード、クライアントまたはサービス プロバイダーは、ローカル メッセージ ストアへの接続をオーバーライドし、リモート サーバー上のストアを開くには MDB_ONLINE でこのメソッドを呼び出すことができます。 同じ MAPI セッションで同時にキャッシュ モードと非キャッシュ モードで、Exchange ストアを開くことができません。 キャッシュされたメッセージ ストアを既に開いている場合、このフラグで開き、またはこのフラグを使用してリモート サーバー上の Exchange ストアを開く新しい MAPI セッションを開始する前にストアを閉じる必要がありますか。
      
  - MDB_TEMPORARY: は、メッセージ ・ ストアは永続的ではありませんし、メッセージ ストアのテーブルに追加できませんする必要があります、MAPI を指示します。 このフラグを使用して、プロファイル セクションから情報をプログラムによって取得できるように、メッセージ ストアにログオンします。 
      
  - MDB_WRITE: 要求読み取り/書き込み、メッセージ ・ ストアにアクセスを許可します。
    
_lppMDB_
  
> [out]メッセージ ・ ストアのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ ・ ストアが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーが十分なアクセス許可を持っているメッセージ ストアにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_で指定されたメッセージ ・ ストアが存在しません。 
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコード ページをサポートするために構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするために構成されていません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しが成功したが、メッセージ ストア プロバイダーが使用可能なエラー情報を持ちます。 この警告が返されると、呼び出しを成功として処理する必要があります。 プロバイダーからエラー情報を取得するには、 [IMAPISession::GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPISession::OpenMsgStore**メソッドは、特定のメッセージ ストアを開きます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ ストアの既定のアクセス許可レベルは、読み取り専用です。 MDB_WRITE フラグを設定した場合、まだ可能性がありますは許可されません読み取り/書き込みアクセス許可。 MAPI の割り当て、メッセージ ・ ストアには、アクセス許可レベルに依存しているアクセスの最後のレベル、メッセージ ・ ストア自体、およびメッセージ ストア プロバイダーです。 
  
読み取り専用アクセス権を持つメッセージ ・ ストアを開くには、 **OpenMsgStore**を呼び出すと、次が発生します。 
  
- 店舗の**PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティには、そのストアがない\_MODIFY_OK とストア\_CREATE_OK ビットをセットします。 
    
- MAPI_MODIFY フラグを設定して[IMAPISession::OpenEntry](imapisession-openentry.md)を使用してメッセージ ストアのメッセージまたはフォルダーのいずれかを開く呼び出しは失敗します。 
    
- MAPI_MODIFY フラグを使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を使用してメッセージ ストアのメッセージまたはフォルダーのプロパティのいずれかを開く呼び出しは失敗します。 
    
- 次の方法のいずれかの呼び出しは失敗します。 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- コピーしたメッセージの送信先は、読み取り専用でリンク先が元のメッセージ ストアの場合と同じまたは別の読み取り専用ストアは、かどうかの場合、次のメソッドへの呼び出しは失敗します。
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI では、 **IMAPISession::OpenMsgStore**メソッドを使用して、メッセージ ストアを開けません。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
- [エラー処理のためのマクロを使用してください。](using-macros-for-error-handling.md)

