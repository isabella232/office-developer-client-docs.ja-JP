---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409336"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイスポインターを返します。 
  
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数 _。_
    
 _lて tryid_
  
> 順番開くオブジェクトのエントリ識別子へのポインター。または NULL。 _lな tryid_が NULL に設定されている場合、 **openentry**はメッセージストアのルートフォルダーを開きます。 
    
 _lpinterface_
  
> 順番開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 オブジェクトの標準インターフェイス (フォルダーの[imapifolder](imapifolderimapicontainer.md)およびメッセージの[IMessage](imessageimapiprop.md) ) が返されると、NULL 結果が渡されます。 
    
 _ulFlags_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを使用できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに対して許可されている最大のネットワークアクセス許可、およびクライアントアプリケーションの最大アクセスを使用して、オブジェクトを開くように要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合は、読み取り専用アクセス許可を使用してオブジェクトを開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のクライアントがオブジェクトを完全に使用できるようになる前に、 **openentry**が正常に返されることを許可します。 オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを使用することはできません。 
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたか、またはユーザーが十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。
    
MAPI_NO_CACHE
  
> ストアをキャッシュモードで開くと、クライアントまたはサービスプロバイダーは**IMsgStore:: openentry**を呼び出し、MAPI_NO_CACHE フラグを設定して、リモートストアのアイテムまたはフォルダーを開くことができます。 リモートサーバーの MDB_ONLINE フラグを使用してメッセージストアを開いた場合、MAPI_NO_CACHE フラグを使用する必要はありません。
    
## <a name="remarks"></a>注釈

**IMsgStore:: openentry**メソッドは、フォルダーまたはメッセージを開き、さらにアクセスするために使用できるインターフェイスへのポインターを返します。 
  
> [!IMPORTANT]
> フォルダーやメッセージなどのパブリックストアでフォルダーエントリを開くときは、 [imapisession:: openentry](imapisession-openentry.md)の代わりに**IMsgStore:: openentry**を使用します。 これにより、プロファイルに複数の Exchange アカウントが定義されている場合に、パブリックフォルダーが正しく機能することが保証されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定しない限り、フォルダーとメッセージは読み取り専用アクセス許可で自動的に開かれます。 これらのフラグのいずれかを設定しても、特定の種類のアクセス許可は保証されません。付与されるアクセス許可は、メッセージストアプロバイダー、アクセスレベル、およびオブジェクトによって異なります。 開いているオブジェクトのアクセスレベルを確認するには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。
  
**IMsgStore:: openentry**を使用して任意のフォルダーまたはメッセージを開くことができますが、開くフォルダーまたはメッセージの親フォルダーにアクセスできる場合は、通常、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)メソッドを使用する方が高速です。 
  
_lpulobjtype_パラメーターで返された値を調べて、返されたオブジェクトの種類が予想どおりであるかどうかを確認します。 オブジェクトの種類が想定された型ではない場合は、ポインターを_lppunk_パラメーターから適切な型のポインターにキャストします。 たとえば、フォルダーを開いている場合は、 **LPMAPIFOLDER**型のポインターに_lppunk_をキャストします。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |callopenentry  <br/> |mfcmapi は、 **IMsgStore:: openentry**メソッドを使用して、エントリ ID に関連付けられているオブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

