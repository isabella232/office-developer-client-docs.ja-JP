---
title: IAddrBookOpenEntry
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
description: '�ŏI�X�V��: 2013�N2��1��'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800394"
---
# <a name="iaddrbookopenentry"></a>アドレス帳コンテナー

**適用されます**: Outlook 
  
アドレス帳エントリを開き、エントリにアクセスするために使用するインターフェイスへのポインターを返します。
  
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

## <a name="parameters"></a>Parameters

_cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
_lpEntryID_
  
> [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。
    
_lpInterface_
  
> [in][Open] エントリにアクセスするために使用するインターフェイスのインターフェイス id (IID) へのポインター。 NULL を渡すと、オブジェクトの標準的なインターフェイスが返されます。 メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。 配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)は、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。 呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。 
    
_ulFlags_
  
> [in]エントリを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_BEST_ACCESS 
  
> 最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。 たとえば、クライアントに読み取り/書き込み権限がある場合は、アドレス帳プロバイダーは、読み取り/書き込みアクセス許可を持つエントリを開くしようとします。 クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得するに与えられたアクセス レベルを取得できます。
    
MAPI_CACHE_ONLY
  
> アドレス帳エントリを開き、[キャッシュからのみアクセスすること。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_DEFERRED_ERRORS 
  
> 成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。
    
MAPI_GAL_ONLY
  
> GAL のみを使用して、名前解決を実行します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
  > [!NOTE]
  > _UlFlags_ MAPI_GAL_ONLY は、現在あるダウンロード可能なヘッダー ファイルで定義されていない可能性があります、場合に追加できます、次の値を使用してコード: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> エントリで開くことの要求の読み取り/書き込みのアクセス許可 エントリは、既定で読み取り専用アクセスで開かれるが、ためクライアントを考慮に入れて MAPI_MODIFY が設定されているかどうかに関係なく読み取り/書き込み権限が与えられたことです。
    
MAPI_NO_CACHE
  
> 名前解決を実行するのには、オフライン アドレス帳を使用しません。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
_lpulObjType_
  
> [out]開かれているエントリの種類へのポインター。
    
_lppUnk_
  
> [out]開かれているエントリへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> エントリが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーが十分なアクセス許可を持っているエントリを開くしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_によって表されるエントリが存在しません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_で指定されたエントリの識別子を指定することはありません。 この値は通常、対応するエントリのアドレス帳プロバイダーが開いていない場合に返されます。 
    
## <a name="remarks"></a>Remarks

クライアントおよびサービス プロバイダーを開くには、アドレス帳のエントリの**アドレス帳コンテナー**のメソッドを呼び出します。 MAPI では、 _lpEntryID_パラメーターで渡されたエントリの識別子に含まれる[MAPIUID](mapiuid.md)構造に基づく、適切なアドレス帳プロバイダーへの呼び出しを転送します。 _UlFlags_パラメーターで MAPI_MODIFY または MAPI_BEST_ACCESS フラグが設定されていない場合、アドレス帳プロバイダーには読み取り専用でエントリが開きます。 ただし、これらのフラグは、ご提案します。 アドレス帳プロバイダーが要求されたエントリの変更を許可していない場合は、MAPI_E_NO_ACCESS を返します。 
  
_LpInterface_パラメーターでは、開かれているエントリにアクセスするのにはどのインタ フェースを使用する必要があることを示します。 _LpInterface_に NULL を渡すことを示すエントリの種類の標準的な MAPI インターフェイスを使用する必要があります。 呼び出し側に返されるオブジェクトの型があるかどうかを判断するのには_lpulObjType_パラメーターで返される値をチェックする必要があるため、アドレス帳プロバイダーは、 _lpInterface_パラメーターによって示されたものとは別のインターフェイスを返すことがあります、何が必要です。 型のオブジェクトの種類がない場合は、呼び出し元は_lppUnk_パラメーターより適切な型にキャストできます。 
  
## <a name="see-also"></a>関連項目

- [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

