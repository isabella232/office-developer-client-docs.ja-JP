---
title: imapisessionopenentry
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
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329415"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトを開き、追加のアクセスのためのインターフェイスポインターを返します。
  
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番開くオブジェクトのエントリ識別子へのポインター。
    
 _lpinterface_
  
> 順番開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスが返されます。 たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは[IMessage](imessageimapiprop.md)になります。フォルダーの場合は、 [imapifolder](imapifolderimapicontainer.md)です。 アドレス帳オブジェクトの標準インターフェイスは、配布リストの[idistlist](idistlistimapicontainer.md)で、メッセージングユーザーの[idistlist](imailuserimapiprop.md)です。 
    
 _ulFlags_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを使用できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに対して許可されている最大のネットワークアクセス許可、およびクライアントアプリケーションの最大アクセスを使用して、オブジェクトを開くように要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合、そのオブジェクトは読み取り専用アクセス許可で開かれている必要があります。 
    
MAPI_CACHE_OK
  
> オフラインアドレス帳を含むすべての方法を使用して、名前の解決を行います。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフラインアドレス帳のみを使用します。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のクライアントがオブジェクトを完全に使用できるようになる前に、 **openentry**が正常に返されることを許可します。 オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを使用することはできません。 
    
MAPI_NO_CACHE
  
> オフラインアドレス帳を使用して名前解決を実行しないでください。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムの保存期間内にあるとマークされているアイテムを表示します。
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしました。または、ユーザーが十分な権限を持っていないオブジェクトにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_パラメーターに渡されたエントリ id に関連付けられたオブジェクトがありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_パラメーターで渡されたエントリ id は、認識できない形式です。 通常、この値は、オブジェクトを含むサービスプロバイダーが開かれていない場合に返されます。 
    
## <a name="remarks"></a>解説

**imapisession:: openentry**メソッドは、メッセージストアまたはアドレス帳オブジェクトを開き、オブジェクトへのアクセスに使用できるインターフェイスへのポインターを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

> [!IMPORTANT]
> フォルダーやメッセージなどのパブリックストアでフォルダーエントリを開くときは、 **imapisession:: openentry**の代わりに[IMsgStore:: openentry](imsgstore-openentry.md)を使用します。 これにより、プロファイルに複数の Exchange アカウントが定義されている場合に、パブリックフォルダーが正しく機能することが保証されます。 
  
開くオブジェクトの種類がわからない場合にのみ、 **imapisession:: openentry**のみを呼び出します。 フォルダーまたはメッセージを開こうとしていることがわかっている場合は、 [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出します。 アドレス帳コンテナー、メッセージングユーザー、または配布リストを開いていることがわかっている場合は、 [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。 これらのより具体的な方法は、 **imapisession:: openentry**よりも高速です。 
  
MAPI では、 _ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定しない限り、読み取り専用アクセス許可を持つすべてのオブジェクトが開かれます。 これらのフラグのいずれかを設定しても、特定の種類のアクセス権は保証されません。付与されるアクセス許可は、サービスプロバイダー、アクセスレベル、およびオブジェクトによって異なります。 開いているオブジェクトのアクセスレベルを確認するには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。
  
**imapisession:: openentry**を呼び出し、メッセージストアのエントリ識別子をポイントするように_lMDB_NO_DIALOG tryid_を設定することは、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドをフラグセットを指定して呼び出すのと同じです。 フラグの設定も同様ですが、 **openmsgstore**で読み取り/書き込みアクセス許可を要求する場合は、MAPI_MODIFY ではなく MDB_WRITE フラグを設定する必要があります。 
  
_lpulobjtype_パラメーターで返された値を調べて、返されたオブジェクトの種類が期待したものであるかどうかを確認します。 オブジェクトの種類が想定した型ではない場合は、ポインターを_lppunk_パラメーターから適切な型のポインターにキャストします。 たとえば、フォルダーを開いている場合は、LPMAPIFOLDER 型のポインターに_lppunk_をキャストします。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |callopenentry  <br/> |mfcmapi は、 **imapisession:: openentry**メソッドを使用してオブジェクトを開きます。  <br/> |
   
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

