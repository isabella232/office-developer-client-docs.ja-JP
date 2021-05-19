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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426388"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトを開き、追加のアクセス用のインターフェイス ポインターを返します。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]開くオブジェクトのエントリ識別子へのポインター。
    
 _lpInterface_
  
> [in]開いたオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合、オブジェクトの標準インターフェイスが返されます。 たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは [IMessage です](imessageimapiprop.md)。フォルダーの場合 [、IMAPIFolder です](imapifolderimapicontainer.md)。 アドレス帳オブジェクトの標準インターフェイスは、 [配布リストの IDistList、](idistlistimapicontainer.md) メッセージング ユーザー [の IMailUser](imailuserimapiprop.md) です。 
    
 _ulFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを使用できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセスを使用してオブジェクトを開く要求。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用のアクセス許可で開く必要があります。 
    
MAPI_CACHE_OK
  
> 名前解決を実行するには、オフライン アドレス帳を含むすべての手段を使用します。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
MAPI_DEFERRED_ERRORS 
  
> オブジェクトが呼び出し元のクライアントで完全に利用できる前に **、OpenEntry** が正常に返されるのを許可します。 オブジェクトが使用できない場合は、後続のオブジェクト呼び出しを実行するとエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で開き、クライアントは読み取り/書き込みアクセス許可が付与されるという前提で動作しません。 
    
MAPI_NO_CACHE
  
> 名前解決を実行するには、オフライン アドレス帳を使用しない。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
SHOW_SOFT_DELETES
  
> 現在、ソフト削除済みとしてマークされているアイテム (つまり、削除済みアイテムの保持時間フェーズにある) を表示します。
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたか、ユーザーが不十分なアクセス許可を持つオブジェクトにアクセスしようとした。
    
MAPI_E_NOT_FOUND 
  
> lpEntryID パラメーターで渡されたエントリ識別子に関連  _付けられたオブジェクトは含_ めではありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID_ パラメーターで渡されるエントリ識別子は、認識できない形式です。 通常、この値は、オブジェクトを含むサービス プロバイダーが開いていない場合に返されます。 
    
## <a name="remarks"></a>注釈

**IMAPISession::OpenEntry** メソッドは、メッセージ ストアまたはアドレス帳オブジェクトを開き、オブジェクトへのアクセスに使用できるインターフェイスへのポインターを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

> [!IMPORTANT]
> フォルダーやメッセージなどのパブリック ストアでフォルダー エントリを開く場合は **、IMAPISession::OpenEntry** の代わりに [IMsgStore::OpenEntry](imsgstore-openentry.md)を使用します。 これにより、複数のアカウントがプロファイルで定義されている場合Exchangeパブリック フォルダーが正しく機能します。 
  
**IMAPISession::OpenEntry** を呼び出すのは、開いているオブジェクトの種類が分からない場合のみです。 フォルダーまたはメッセージを開いている場合は [、IMsgStore::OpenEntry を呼び出します](imsgstore-openentry.md)。 アドレス帳コンテナー、メッセージング ユーザー、または配布リストを開いている場合は [、IAddrBook::OpenEntry を呼び出します](iaddrbook-openentry.md)。 これらのより具体的なメソッドは **、IMAPISession::OpenEntry よりも高速です**。 
  
MAPI は  _、ulFlags_ パラメーターで MAPI_MODIFYまたはMAPI_BEST_ACCESSを設定しない限り、読み取り専用のアクセス許可を持つすべてのオブジェクトを開きます。 これらのフラグのいずれかを設定しても、特定の種類のアクセスが保証されるという保証はありません。付与されるアクセス許可は、サービス プロバイダー、アクセス レベル、およびオブジェクトによって異なります。 開いたオブジェクトのアクセス レベルを確認するには、そのオブジェクト [(PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md) **PR_ACCESS_LEVELプロパティを** 取得します。
  
**IMAPISession::OpenEntry** を呼び出し _、lpEntryID_ をメッセージ ストアのエントリ識別子をポイントする設定は、MDB_NO_DIALOG フラグセットを使用して [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを呼び出すのと同じです。 また **、OpenMsgStore** で読み取り/書き込みアクセス許可を要求する場合を除き、フラグの設定も同じですが、MDB_WRITE フラグを設定する必要MAPI_MODIFY。 
  
_lpulObjType_ パラメーターで返される値を確認して、返されるオブジェクトの種類が予期した値であるかどうかを確認します。 オブジェクトの種類が予期した型ではない場合は  _、lppUnk_ パラメーターから適切な型のポインターにポインターをキャストします。 たとえば、フォルダーを開く場合は  _、lppUnk_ を LPMAPIFOLDER 型のポインターにキャストします。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI は **IMAPISession::OpenEntry メソッド** を使用してオブジェクトを開きます。  <br/> |
   
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

