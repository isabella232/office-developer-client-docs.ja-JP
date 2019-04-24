---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326348"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番開くオブジェクトのエントリ識別子へのポインター。
    
 _lpinterface_
  
> 順番オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 返されるオブジェクトの標準インターフェイスで NULL 結果が渡されます。 たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは[IMessage](imessageimapiprop.md)になります。フォルダーの場合は、 [imapifolder](imapifolderimapicontainer.md)です。 アドレス帳オブジェクトの標準インターフェイスは、配布リストの[idistlist](idistlistimapicontainer.md)で、メッセージングユーザーの[idistlist](imailuserimapiprop.md)です。 
    
 _ulo・フラグ_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> 呼び出し元に対して許可されている最大のネットワークアクセス許可を使用して、オブジェクトを開くように要求します。 たとえば、呼び出し元に読み取り/書き込みアクセス許可が設定されている場合、オブジェクトは読み取り/書き込みとして開かれる必要があります。呼び出し元が読み取り専用のアクセス許可を持っている場合、そのオブジェクトは読み取り専用として開かれる必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> オブジェクトが呼び出し元から完全にアクセス可能になる前に、 **openentry**が正常に返されることを許可します。 オブジェクトにアクセスできない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用として開かれ、読み取り/書き込みアクセス許可が付与されているという前提で呼び出し元は機能しません。 
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたか、ユーザーが必要なアクセス許可を持っていないオブジェクトへのアクセスが行われました。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_パラメーターに渡されたエントリ id に関連付けられたオブジェクトがありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_パラメーターで渡されたエントリ id は、認識できない形式です。 通常、この値は、オブジェクトを含むアドレス帳プロバイダーが開かれていない場合に返されます。 
    
## <a name="remarks"></a>解説

**imapisupport:: openentry**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは、 **imapisupport:: openentry**を呼び出して、特定のオブジェクトへのアクセスに使用できるインターフェイスへのポインターを取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

開こうとしているオブジェクトの種類がわからない場合は、 **imapisupport:: openentry**のみを呼び出します。 フォルダーまたはメッセージを開いていることがわかっている場合は、代わりに[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出します。 アドレス帳コンテナー、メッセージングユーザー、または配布リストを開いていることがわかっている場合は、 [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。 これらのより具体的な方法は、 **imapisupport:: openentry**よりも高速です。 
  
 **imapisupport:: openentry**は、 _ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定し、アクセス許可が十分でない限り、すべてのオブジェクトを読み取り専用として開きます。 これらのフラグのいずれかを設定しても、特定の種類のアクセス権は保証されません。付与されるアクセス許可は、そのオブジェクトを所有するアクセスレベル、オブジェクト、およびサービスプロバイダーによって異なります。 開いているオブジェクトのアクセスレベルを確認するには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。
  
_lpulobjtype_パラメーターで返された値を調べて、返されたオブジェクトの種類が期待したものであることを確認します。 オブジェクトの種類が想定どおりの場合は、ポインターを_lppunk_パラメーターから適切な型のポインターにキャストします。 たとえば、フォルダーを開いている場合は、LPMAPIFOLDER 型のポインターに_lppunk_をキャストします。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

