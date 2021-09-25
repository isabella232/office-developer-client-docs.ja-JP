---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cd6b0fd6c080e9d8dfe25b5e1a1773bc563efb89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575856"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアを開き、さらにアクセスする [IMsgStore ポインター](imsgstoreimapiprop.md) を返します。 
  
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

## <a name="parameters"></a>パラメーター

_ulUIParam_
  
> [in]共通のアドレス ダイアログ ボックスの親ウィンドウへのハンドルと、その他の関連する表示。
    
_cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
_lpEntryID_
  
> [in]開くメッセージ ストアのエントリ識別子へのポインター。 _lpEntryID パラメーター_ は NULL にすることはできません。 
    
_lpInterface_
  
> [in]メッセージ ストアへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合  _、lppMDB_ パラメーターはメッセージ ストア **(IMsgStore)** の標準インターフェイスへのポインターを返します。
    
_ulFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを使用できます。
    
  - MAPI_BEST_ACCESS: ユーザーに許可される最大ネットワークアクセス許可とクライアント アプリケーションの最大アクセス許可を使用してメッセージ ストアを開く要求。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、メッセージ ストアを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、メッセージ ストアを読み取り専用のアクセス許可で開く必要があります。 
      
  - MAPI_DEFERRED_ERRORS: メッセージ ストアが呼び出し元のクライアントで完全に利用できる前に **、OpenMsgStore** が正常に返されるのを許可します。 メッセージ ストアを使用できない場合は、後続のオブジェクト呼び出しを実行するとエラーが発生する可能性があります。 
      
  - MDB \_ NO_DIALOG: ログオン ダイアログ ボックスの表示を防止します。 このフラグが設定されている場合 **、OpenMsgStore** には、ユーザーの助けを借りずにメッセージ ストアを開くのに十分な構成情報がない場合は、メッセージ ストアMAPI_E_LOGON_FAILED。 このフラグが設定されていない場合、メッセージ ストア プロバイダーは、名前またはパスワードを修正するか、メッセージ ストアへの接続を確立するために必要なその他のアクションを実行するようにユーザーに求められます。 
      
  - MDB NO_MAIL: メッセージ ストアは、 \_ メールの送受信には使用できません。 このフラグが設定されている場合、MAPI は、このメッセージ ストアが開いているという MAPI スプーラーに通知されません。
      
  - MDB ONLINE: キャッシュ Exchange モードでは、クライアントまたはサービス プロバイダーは MDB_ONLINE でこのメソッドを呼び出して、ローカル メッセージ ストアへの接続をオーバーライドし、リモート サーバー上でストアを開きます。 \_ 同じ MAPI セッションExchangeキャッシュ モードと非キャッシュ モードで、キャッシュ ストアを開くことができません。 キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。
      
  - MDB_TEMPORARY: メッセージ ストアが永続的ではなく、メッセージ ストア テーブルに追加しないよう MAPI に指示します。 このフラグは、メッセージ ストアにログオンするために使用され、プロファイル セクションからプログラムによって情報を取得できます。 
      
  - MDB_WRITE: メッセージ ストアへの読み取り/書き込みアクセス許可を要求します。
    
_lppMDB_
  
> [out]メッセージ ストアのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ ストアが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーのアクセス許可が不十分なメッセージ ストアにアクセスしようとした。
    
MAPI_E_NOT_FOUND 
  
> _lpEntryID_ で示されるメッセージ ストアが存在しません。 
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコード ページをサポートするように構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするように構成されていません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、メッセージ ストア プロバイダーにエラー情報が表示されます。 この警告が返されると、呼び出しは正常に処理されます。 プロバイダーからエラー情報を取得するには [、IMAPISession::GetLastError メソッドを呼び出](imapisession-getlasterror.md) します。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPISession::OpenMsgStore** メソッドは、特定のメッセージ ストアを開きます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ ストアの既定のアクセス許可レベルは読み取り専用です。 このフラグを設定MDB_WRITE、引き続き読み取り/書き込みアクセス許可が付与されない場合があります。 MAPI がメッセージ ストアに割り当てるアクセスの最終レベルは、アクセス許可レベル、メッセージ ストア自体、およびメッセージ ストア プロバイダーによって異なります。 
  
**OpenMsgStore を呼び出して** 読み取り専用のアクセス許可を持つメッセージ ストアを開く場合、次の処理が行われます。 
  
- ストアの **PR \_** STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティには、STORE の値と STORE MODIFY_OKが設定 \_ \_ CREATE_OKされません。 
    
- [IMAPISession::OpenEntry](imapisession-openentry.md)を使用してメッセージ ストアのメッセージまたはフォルダーの 1 つを開く呼び出しは、MAPI_MODIFYが失敗します。 
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を使用してメッセージ ストアのメッセージまたはフォルダーのプロパティの 1 つを開く呼び出しは、MAPI_MODIFY失敗します。 
    
- 次のメソッドの呼び出しは失敗します。 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- コピー先がソース メッセージ ストアと同じか、別の読み取り専用ストアである場合でも、コピーされたメッセージの送信先が読み取り専用の場合、次のメソッドの呼び出しは失敗します。
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI は **IMAPISession::OpenMsgStore** メソッドを使用してメッセージ ストアを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
- [エラー処理にマクロを使用する](using-macros-for-error-handling.md)

