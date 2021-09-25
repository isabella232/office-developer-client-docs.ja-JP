---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: '最終更新日: 2013 年 2 月 1 日'
ms.openlocfilehash: b1b6ebd5e7d1ad30e9cc0ef2ad4c706dac6788b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561573"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。
  
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
  
> [in]開くアドレス帳エントリを表すエントリ識別子へのポインター。
    
_lpInterface_
  
> [in]開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合、オブジェクトの標準インターフェイスが返されます。 メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。 配布リストの場合 [、IDistList : IMAPIContainer](idistlistimapicontainer.md) であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。 呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
_ulFlags_
  
> [in]エントリの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> 許可されるネットワークおよびクライアントの最大アクセス許可を使用してエントリを開くことを要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、アドレス帳プロバイダーは読み取り/書き込みアクセス許可を持つエントリを開く必要があります。 クライアントは、開いているエントリの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し **、PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することで、付与されたアクセス レベルを取得できます。
    
MAPI_CACHE_ONLY
  
> アドレス帳エントリを開き、キャッシュからのみアクセスします。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
MAPI_DEFERRED_ERRORS 
  
> エントリが完全に開いて使用可能になる前に、呼び出しが成功する可能性があります。後でエントリを呼び出してもエラーが返される可能性があります。
    
MAPI_GAL_ONLY
  
> 名前解決を実行するには、GAL のみを使用します。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
  > [!NOTE]
  > _ulFlags_ MAPI_GAL_ONLYは、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を持つエントリを開く要求。 既定では、読み取り専用アクセスでエントリが開くので、クライアントは、読み取り/書き込みアクセス許可が設定されているかどうかに関係なく、読み取り/書き込み権限が付与MAPI_MODIFY必要があります。
    
MAPI_NO_CACHE
  
> 名前解決を実行するには、オフライン アドレス帳を使用しない。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
_lpulObjType_
  
> [out]開いたエントリの種類へのポインター。
    
_lppUnk_
  
> [out]開いたエントリへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エントリが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーのアクセス許可が不十分なエントリを開く試みがあった。
    
MAPI_E_NOT_FOUND 
  
> _lpEntryID で表されるエントリ_ が存在しません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID で指定されたエントリ識別子_ は認識されません。 通常、この値は、対応するエントリを担当するアドレス帳プロバイダーが開いていない場合に返されます。 
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **、IAddrBook::OpenEntry** メソッドを呼び出してアドレス帳エントリを開きます。 MAPI は _、lpEntryID_ パラメーターで渡されたエントリ識別子に含まれる [MAPIUID](mapiuid.md)構造に基づいて、適切なアドレス帳プロバイダーに呼び出しを転送します。 アドレス帳プロバイダーは  _、ulFlags_ パラメーターの MAPI_MODIFYまたは MAPI_BEST_ACCESSフラグが設定されていない限り、読み取り専用としてエントリを開きます。 ただし、これらのフラグは提案です。 アドレス帳プロバイダーが要求されたエントリの変更を許可しない場合は、アドレス帳プロバイダーはMAPI_E_NO_ACCESS。 
  
_lpInterface パラメーター_ は、開かれたエントリにアクセスするために使用するインターフェイスを示します。 _lpInterface で NULL を渡す_ 場合は、その種類のエントリの標準 MAPI インターフェイスを使用する必要があることを示します。 アドレス帳プロバイダーは  _、lpInterface_ パラメーターによって提案されたインターフェイスとは異なるインターフェイスを返す可能性があるため、呼び出し元は  _lpulObjType_ パラメーターで返された値を確認して、返されるオブジェクトの種類が予期した値であるかどうかを判断する必要があります。 オブジェクトの種類が予期される型ではない場合、呼び出し元は  _lppUnk_ パラメーターを、より適切な型にキャストできます。 
  
## <a name="see-also"></a>関連項目

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

