---
title: imapisessionopenmsgstore
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325768"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。 
  
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

_uluiparam_
  
> 順番[共通アドレス] ダイアログボックスとその他の関連する表示の親ウィンドウへのハンドル。
    
_cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
_lて tryid_
  
> 順番開くメッセージストアのエントリ識別子へのポインター。 _lな tryid_パラメーターを NULL にすることはできません。 
    
_lpinterface_
  
> 順番メッセージストアへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、 _lppmdb_パラメーターによって、メッセージストア (**IMsgStore**) の標準インターフェイスへのポインターが返されます。
    
_ulFlags_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを使用できます。
    
  - MAPI_BEST_ACCESS: ユーザーに対して許可される最大のネットワークアクセス許可、および最大クライアントアプリケーションのアクセス許可を使用して、メッセージストアを開くように要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可でメッセージストアを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合は、メッセージストアを読み取り専用アクセス許可で開く必要があります。 
      
  - MAPI_DEFERRED_ERRORS: **openmsgstore**が正常に復帰することを許可します。これは、メッセージストアが呼び出し元クライアントに完全に使用可能になる前である可能性があります。 メッセージストアが使用できない場合は、後続のオブジェクト呼び出しを行うとエラーが発生する可能性があります。 
      
  - MDB\_NO_DIALOG: ログオンダイアログボックスが表示されないようにします。 このフラグが設定されており、 **openmsgstore**の構成情報が不足しているために、ユーザーのヘルプなしでメッセージストアを開くことができない場合は、MAPI_E_LOGON_FAILED が返されます。 このフラグが設定されていない場合、メッセージストアプロバイダーは、ユーザーに対して名前またはパスワードを修正するか、またはメッセージストアへの接続を確立するために必要なその他のアクションを実行するように求めることができます。 
      
  - MDB\_NO_MAIL: メールを送信または受信するときに、メッセージストアを使用することはできません。 このフラグが設定されている場合、mapi は、このメッセージストアが開かれていることを mapi スプーラーに通知しません。
      
  - MDB\_ONLINE: Exchange キャッシュモードでは、クライアントまたはサービスプロバイダーは、MDB_ONLINE を使用してこのメソッドを呼び出して、ローカルメッセージストアへの接続を上書きし、リモートサーバー上でストアを開くことができます。 同じ MAPI セッションで、キャッシュモードおよび非キャッシュモードでは、Exchange ストアを同時に開くことはできません。 キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。
      
  - MDB_TEMPORARY: MAPI に、メッセージストアが永続的ではなく、メッセージストアテーブルに追加されないようにするように指示します。 このフラグは、メッセージストアにログオンして、プロファイルセクションからプログラムによって情報を取得できるようにするために使用されます。 
      
  - MDB_WRITE: メッセージストアへの読み取り/書き込みアクセス許可を要求します。
    
_lppmdb_
  
> 読み上げメッセージストアのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージストアが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーが十分なアクセス許可を持っていないメッセージストアにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_で示されたメッセージストアが存在しません。 
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコードページをサポートするように構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするように構成されていません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、メッセージストアプロバイダーにエラー情報があります。 この警告が返された場合、呼び出しは正常に処理されます。 プロバイダーからエラー情報を取得するには、 [imapisession:: GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapisession:: openmsgstore**メソッドは、特定のメッセージストアを開きます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージストアの既定のアクセス許可レベルは、読み取り専用です。 MDB_WRITE フラグを設定しても、読み取り/書き込みアクセス許可が与えられない場合があります。 MAPI がメッセージストアに割り当てる最終レベルのアクセス権は、アクセス許可レベル、メッセージストア自体、およびメッセージストアプロバイダーによって異なります。 
  
**openmsgstore**を呼び出して、読み取り専用のアクセス許可でメッセージストアを開くと、次のようになります。 
  
- ストアの**PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティには、ストア\_MODIFY_OK および store\_CREATE_OK bits が設定されていません。 
    
- MAPI_MODIFY フラグが設定された[openentry:: imapisession](imapisession-openentry.md)を使用して、メッセージストアのメッセージまたはフォルダーの1つを開くための呼び出しは失敗します。 
    
- MAPI_MODIFY フラグが設定された[imapiprop:: openproperty](imapiprop-openproperty.md)を使用して、メッセージストアのメッセージまたはフォルダーのプロパティの1つを開くための呼び出しは失敗します。 
    
- 次のいずれかのメソッドへの呼び出しは失敗します。 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- コピー先がソースメッセージストアと同じかどうか、または別の読み取り専用ストアであるかどうかにかかわらず、コピーされたメッセージの転送先が読み取り専用である場合、次のメソッドの呼び出しは失敗します。
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIStoreFunctions  <br/> |callopenmsgstore  <br/> |mfcmapi は、 **imapisession:: openmsgstore**メソッドを使用して、メッセージストアを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
- [エラー処理にマクロを使用する](using-macros-for-error-handling.md)

