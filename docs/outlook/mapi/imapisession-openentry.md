---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f23b4855b7e2faeb599868f8c2db52ae9cbfbfd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800687"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**適用対象**: Outlook 
  
オブジェクトを開き、追加のアクセスのインターフェイス ポインターを返します。
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはオブジェクトのエントリの識別子へのポインター。
    
 _lpInterface_
  
> [in]開かれているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準的なインターフェイスが返されます。 などのオブジェクトを開くことができませんが、メッセージの場合は、標準のインタ フェースは、 [IMessage](imessageimapiprop.md)です。フォルダー、 [IMAPIFolder](imapifolderimapicontainer.md)です。 アドレス帳オブジェクトの標準的なインターフェイスは、配布リストおよび[IMailUser](imailuserimapiprop.md)のメッセージング ユーザーの[IDistList](idistlistimapicontainer.md)です。 
    
 _ulFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを使用することができます。
    
MAPI_BEST_ACCESS 
  
> ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を使用して、オブジェクトを開くことを要求します。 たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用権限を持つオブジェクトを開く必要があります。 
    
MAPI_CACHE_OK
  
> オフライン アドレス帳を含め、すべての手段を使用すると、名前解決を実行できます。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するのにには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_DEFERRED_ERRORS 
  
> **OpenEntry**を正常に戻す、可能性のあるオブジェクトが呼び出し元のクライアントに完全に利用できる前にするにを使用できます。 オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生することができます。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用の権限を持つオブジェクトが開いているし、クライアントが読み取り/書き込み権限が与えられていることを前提に動作しない必要があります。 
    
MAPI_NO_CACHE
  
> 名前解決を実行するのには、オフライン アドレス帳を使用しません。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
SHOW_SOFT_DELETES
  
> ソフトとしてマークされているアイテムの削除を表示する (つまりにいる削除済みアイテムの保存時間フェーズ)。
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしましたまたは、ユーザーが十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_パラメーターで渡されたエントリの識別子に関連付けられているオブジェクトではありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_パラメーターで渡されたエントリ id が、認識できない形式です。 この値は通常、オブジェクトが含まれているサービス プロバイダーが開いていない場合に返されます。 
    
## <a name="remarks"></a>注釈

メッセージが保存、またはアドレス帳オブジェクト、インターフェイスへのポインターを返す**IMAPISession::OpenEntry**メソッドが表示は、オブジェクトへのアクセスに使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

> [!IMPORTANT]
> フォルダーやメッセージなどのパブリック ストア上のフォルダーのエントリを開くときは、 **IMAPISession::OpenEntry**の代わりに[IMsgStore::OpenEntry](imsgstore-openentry.md)を使用します。 これにより、そのパブリック フォルダー関数正しく複数の Exchange アカウントは、プロファイルで定義されている場合。 
  
開こうとしているオブジェクトの種類がわからない場合にのみ、 **IMAPISession::OpenEntry**を呼び出します。 フォルダーまたはメッセージを開いていることがわかっている場合は、 [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 アドレス帳コンテナーである、メッセージング ユーザー、または配布リストが置かれていることがわかっている場合は、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 これらの具体的な方法は、 **IMAPISession::OpenEntry**よりも高速です。 
  
MAPI は、 _ulFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグを設定する場合を除き、読み取り専用のアクセス許可を持つすべてのオブジェクトを開きます。 これらのフラグのいずれかを設定では特定の種類のアクセスは保証されません。与えられたアクセス許可は、サービス プロバイダー、アクセス レベル、およびオブジェクトによって異なります。 開かれたオブジェクトのアクセス レベルを決定するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得します。
  
メッセージ ストアのエントリ id を指すように**IMAPISession::OpenEntry**と_lpEntryID_の設定を呼び出すことは MDB_NO_DIALOG フラグを指定して[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを呼び出す場合と同じ設定します。 フラグの設定も同等ですが、 **OpenMsgStore**と読み取り/書き込みアクセス許可を要求することを除いては、MAPI_MODIFY の代わりに MDB_WRITE フラグを設定する必要があります。 
  
返されるオブジェクトの型は、何が必要かどうかを判断するのには_lpulObjType_パラメーターで返される値を確認してください。 オブジェクトの型が予測した型でない場合は、 _lppUnk_パラメーターの適切な型のポインターへのポインターをキャストします。 などのフォルダーを開いている場合は、LPMAPIFOLDER の型のポインターに_lppUnk_をキャストします。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI では、 **IMAPISession::OpenEntry**メソッドを使用して、オブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

