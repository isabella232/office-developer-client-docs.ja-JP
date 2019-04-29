---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434341"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ機能を実行します。ただし、 _pEmsmdbUID_パラメーターとして従来の**emsmdbUID**を使用する点が異なります。 [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)の呼び出しに対して正しい**emsmdbUID**を取得できない場合は、この関数を使用しないでください。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp .h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _pmsess_
  
> 順番ログオンしている**imapisession**。 NULL にすることはできません。
    
 _pAddrBook_
  
> 順番エントリ識別子を開くために使用されるアドレス帳。 NULL にすることはできません。
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。 
    
 _lて tryid_
  
>  順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。 
    
 _lpinterface_
  
> 順番開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスが返されます。 メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。 配布リストの場合、これは[idistlist: IMAPIContainer](idistlistimapicontainer.md)で、コンテナーの場合は[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)です。 呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
 _ulFlags_
  
> 順番エントリが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS
  
> 許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。 たとえば、クライアントが読み取りおよび書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは、読み取りおよび書き込みアクセス許可を持つエントリを開こうとします。 クライアントは、開いているエントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することによって付与されたアクセスレベルを取得できます。 
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するのにオフラインアドレス帳のみを使用します。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
MAPI_DEFERRED_ERRORS
  
> 呼び出しが正常に完了します。エントリが完全に開かれて使用可能になる前に、エントリへの以降の呼び出しでエラーが返される可能性があることを意味します。
    
MAPI_GAL_ONLY
  
> 名前解決を実行するには、GAL のみを使用します。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
MAPI_MODIFY
  
> 読み取りと書き込みのアクセス許可を使用して、エントリを開くように要求します。 既定では、エントリは読み取り専用アクセスで開かれるため、クライアントは、MAPI_MODIFY が設定されているかどうかに関係なく、読み取りおよび書き込みアクセス許可が付与されたことを想定する必要はありません。
    
MAPI_NO_CACHE
  
> では、オフラインアドレス帳を使用して名前解決を実行しません。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
 _lpulobjtype_
  
> 読み上げ開かれた項目の種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれたエントリのポインターへのポインター。
    

