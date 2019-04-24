---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347790"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**pEmsmdbUID**によって識別される Exchange アドレス帳を使用して、 **entryID**を開きます。 この関数は、 [IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。ただし、この関数を使用すると、予期される Exchange アドレス帳プロバイダーを使用して[IAddrBook:: openentry](iaddrbook-openentry.md)が開かれることが保証されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp .h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _pmsess_
  
> 順番ログオンしている**imapisession**。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> 順番この関数がエントリ識別子の詳細を表示するために使用する exchange アドレス帳プロバイダーを含む exchange サービスを識別する**emsmdbUID**へのポインター。 受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)のように動作します。 このパラメーターが NULL またはゼロ MAPIUID の場合、この関数は[IAddrBook::D etails](iaddrbook-details.md)のように動作します。
    
 _pAddrBook_
  
> 順番エントリ識別子を開くために使用されるアドレス帳。 NULL にすることはできません。
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。 
    
 _lて tryid_
  
>  順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。 
    
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
    

