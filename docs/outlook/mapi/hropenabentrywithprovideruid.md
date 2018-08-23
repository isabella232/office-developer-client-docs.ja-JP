---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800303"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**適用対象**: Outlook 
  
_PEmsabpUID_によって識別される、Exchange アドレス帳を使用して**エントリ Id**が表示されます。 この関数は、この関数を使用すると、予想される Exchange アドレス帳プロバイダーを使用して[アドレス帳コンテナー](iaddrbook-openentry.md)が開かれていることを除いてに、[アドレス帳コンテナー](iaddrbook-openentry.md)同様に動作します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
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

 _pEmsmdbUID_
  
> [in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。 受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。 このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。
    
 _pAddrBook_
  
> [in]アドレス帳のエントリ id を開くために使用します。 NULL にすることはできません。
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
>  [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。 
    
 _lpInterface_
  
> [in][Open] エントリにアクセスするために使用されるインターフェイスのインターフェイス id (IID) へのポインター。 NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。 メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。 配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)は、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。 呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。 
    
 _ulFlags_
  
> [in]方法を制御するフラグのビットマスクのエントリを開いて、次のフラグを設定することができます。
    
MAPI_BEST_ACCESS
  
> 最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。 などの場合、クライアントでは、読み取りし、書き込みのアクセス許可、アドレス帳プロバイダーしようと読み取りでエントリを開き、書き込みのアクセス許可。 クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得するが許可されているアクセス レベルを取得できます。 
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するのにには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_DEFERRED_ERRORS
  
> 成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。
    
MAPI_GAL_ONLY
  
> GAL のみを使用して、名前解決を実行します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_MODIFY
  
> エントリで開くことの要求は、アクセス許可を読み書きします。 エントリは読み取り専用アクセスで開くとき、既定であるために読み書き権限が与えられている MAPI_MODIFY が設定されているかどうかに関係なくクライアントを想定しません。
    
MAPI_NO_CACHE
  
> 名前解決を実行するのには、オフライン アドレス帳を使用しません。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
 _lpulObjType_
  
> [out]開かれているエントリの種類へのポインター。
    
 _lppUnk_
  
> [out]開かれているエントリのポインターへのポインター。
    

