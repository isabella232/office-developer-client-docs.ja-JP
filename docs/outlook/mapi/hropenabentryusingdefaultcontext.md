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
  
従来の _emsmdbUID を pEmsmdbUID_ パラメーターとして使用する以外は [、HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ関数を実行します。 [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)の呼び出しに対して正しい **emsmdbUID** を取得できない場合は、この関数を使用しません。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]ログオンしている **IMAPISession**。 NULL にすることはできません。
    
 _pAddrBook_
  
> [in]エントリ識別子を開くのに使用するアドレス帳。 NULL にすることはできません。
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。 
    
 _lpEntryID_
  
>  [in]開くアドレス帳エントリを表すエントリ識別子へのポインター。 
    
 _lpInterface_
  
> [in]開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。 メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。 配布リストの場合は [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。 呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
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
    
 _lpulObjType_
  
> [out]開いたエントリの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたエントリのポインターへのポインター。
    

