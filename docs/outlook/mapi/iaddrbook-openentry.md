---
title: iaddrbookopenentry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: '最終更新日: 2013 年 2 月 1 日'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287022"
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
_lて tryid_
  
> 順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。
    
_lpinterface_
  
> 順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスが返されます。 メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。 配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。 呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
_ulFlags_
  
> 順番エントリが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> 許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。 たとえば、クライアントが読み取り/書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは読み取り/書き込みアクセス許可でエントリを開こうとする必要があります。 クライアントは、open エントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することによって付与されたアクセスレベルを取得できます。
    
MAPI_CACHE_ONLY
  
> アドレス帳エントリを開き、キャッシュからのみアクセスします。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出しが正常に終了し、エントリが完全に開かれて使用可能になる前に、エントリを後で呼び出すとエラーが返される可能性があることを示すことができます。
    
MAPI_GAL_ONLY
  
> 名前解決を実行するには、GAL のみを使用します。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
  > [!NOTE]
  > _ulflags_ MAPI_GAL_ONLY は、現在のダウンロード可能なヘッダーファイルでは定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を使用してエントリが開かれるように要求します。 既定では、エントリは読み取り専用アクセスで開かれるので、MAPI_MODIFY が設定されているかどうかに関係なく、クライアントは読み取り/書き込みアクセス許可が付与されたことを想定してはなりません。
    
MAPI_NO_CACHE
  
> オフラインアドレス帳を使用して名前解決を実行しないでください。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
_lpulobjtype_
  
> 読み上げ開かれた項目の種類へのポインター。
    
_lppunk_
  
> 読み上げ開かれたエントリへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エントリが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーが十分なアクセス許可を持っていないエントリを開こうとしました。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_で表されるエントリは存在しません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_で指定されているエントリ識別子が認識されません。 この値は、対応するエントリを担当するアドレス帳プロバイダーが開かれていない場合に、通常返されます。 
    
## <a name="remarks"></a>解説

クライアントおよびサービスプロバイダーは、アドレス帳のエントリを開くために**IAddrBook:: openentry**メソッドを呼び出します。 MAPI は、 _lMAPIUID tryid_パラメーターで渡されたエントリ識別子に含まれている[](mapiuid.md)構造に基づいて、適切なアドレス帳プロバイダーに呼び出しを転送します。 MAPI_MODIFY または MAPI_BEST_ACCESS フラグが設定されている場合を除いて、アドレス帳プロバイダー __ はエントリを読み取り専用として開きます。 ただし、これらのフラグは推奨事項です。 アドレス帳プロバイダーで、要求されたエントリの変更が許可されていない場合は、MAPI_E_NO_ACCESS が返されます。 
  
_lpinterface_パラメーターは、開いているエントリへのアクセスに使用するインターフェイスを示します。 _lpinterface_で NULL を渡すことは、そのエントリの種類に対して標準の MAPI インターフェイスが使用されることを示します。 アドレス帳プロバイダーは_lpinterface_パラメーターで提案されたインターフェイスとは異なるインターフェイスを返す可能性があるため、発信者は_lpulobjtype_パラメーターで返された値を確認して、返されるオブジェクトの種類がどうかを判断する必要があります。予想される動作 オブジェクトの種類が想定された型ではない場合、呼び出し元は、 _lppunk_パラメーターをより適切な型にキャストできます。 
  
## <a name="see-also"></a>関連項目

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

