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
ms.openlocfilehash: e0b6718345588e79a8038f7cb409ef901d7c11f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577157"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**PEmsmdbUID**によって識別される、Exchange アドレス帳を使用して**エントリ Id**が表示されます。 この関数は、予想される Exchange アドレス帳プロバイダーを使用して、[アドレス帳コンテナー](iaddrbook-openentry.md)を開くことにより、この関数を使用することを除いて[IAddrBook::Details](iaddrbook-details.md)に同様に動作します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]**IMAPISession**にログオンします。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> [in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。 受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。 このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。
    
 _pAddrBook_
  
> [in]アドレス帳のエントリ id を開くために使用します。 NULL にすることはできません。
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
>  [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。 
    
 _ulFlags_
  
> [in]エントリを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_BEST_ACCESS
  
> 最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。 などの場合、クライアントでは、読み取りし、書き込みのアクセス許可、アドレス帳プロバイダーしようと読み取りでエントリを開き、書き込みのアクセス許可。 クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得するが許可されているアクセス レベルを取得できます。 
    
MAPI_CACHE_ONLY
  
> オフライン アドレス帳のみを使用すると、名前解決を実行します。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_DEFERRED_ERRORS
  
> 成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。
    
MAPI_GAL_ONLY
  
> GAL のみを使用すると、名前解決を実行します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_MODIFY
  
> エントリで開くことの要求は、アクセス許可を読み書きします。 エントリは読み取り専用アクセスで開くとき、既定であるために読み書き権限が与えられている MAPI_MODIFY が設定されているかどうかに関係なくクライアントを想定しません。
    
MAPI_NO_CACHE
  
> 名前解決を実行するのには、オフライン アドレス帳を使用しません。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    

