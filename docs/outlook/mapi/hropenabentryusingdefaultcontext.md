---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 74660de551d43c589cb903b5c3852136f2f18269
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800307"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**適用されます**: Outlook 
  
_PEmsmdbUID_パラメーターとして従来の**emsmdbUID**を使用する[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ機能を実行します。 [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)への呼び出しの正しい**emsmdbUID**を取得することはできない場合に、この関数を使用しません。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _pmsess_
  
> [in]**IMAPISession**にログオンします。 NULL にすることはできません。
    
 _pAddrBook_
  
> [in]アドレス帳のエントリ id を開くために使用します。 NULL にすることはできません。
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
>  [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。 
    
 _lpInterface_
  
> [in][Open] エントリにアクセスするために使用されるインターフェイスのインターフェイス id (IID) へのポインター。 NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。 メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。 配布リストには、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)とは、コンテナーの[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。 呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。 
    
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
    
 _lpulObjType_
  
> [out]開かれているエントリの種類へのポインター。
    
 _lppUnk_
  
> [out]開かれているエントリのポインターへのポインター。
    

