---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434054"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**pEmsmdbUID** で識別Exchangeアドレス帳を使用して entryID を開きます。  この関数は[、IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが、この関数を使用すると[、IAddrBook::OpenEntry](iaddrbook-openentry.md)が予期される Exchange アドレス帳プロバイダーを使用して開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]ログオンしている **IMAPISession**。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> [in]この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを含む Exchange サービスを識別する **emsmdbUID** へのポインター。 受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出し[は IAddrBook::D etails](iaddrbook-details.md)のように動作します。 このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。
    
 _pAddrBook_
  
> [in]エントリ識別子を開くのに使用するアドレス帳。 NULL にすることはできません。
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。 
    
 _lpEntryID_
  
>  [in]開くアドレス帳エントリを表すエントリ識別子へのポインター。 
    
 _ulFlags_
  
> [in]エントリの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS
  
> 許可されるネットワークおよびクライアントの最大アクセス許可を使用してエントリを開くことを要求します。 たとえば、クライアントに読み取りおよび書き込みアクセス許可がある場合、アドレス帳プロバイダーは読み取りおよび書き込みアクセス許可を持つエントリを開きます。 クライアントは、開いているエントリの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することで、付与されたアクセス レベルを取得できます。 
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
MAPI_DEFERRED_ERRORS
  
> エントリが完全に開いて使用可能になる前に、呼び出しが成功する可能性があります。その後のエントリへの呼び出しがエラーを返す可能性を示します。
    
MAPI_GAL_ONLY
  
> 名前解決を実行する場合は、GAL のみを使用します。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
MAPI_MODIFY
  
> 読み取りおよび書き込みアクセス許可を持つエントリを開くことを要求します。 既定では、読み取り専用アクセスでエントリが開くので、クライアントは、読み取りアクセス許可と書き込みアクセス許可が設定されているかどうかに関係なく、読み取りおよび書き込み権限が付与MAPI_MODIFY必要があります。
    
MAPI_NO_CACHE
  
> 名前解決を実行するためにオフライン アドレス帳を使用しない。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    

