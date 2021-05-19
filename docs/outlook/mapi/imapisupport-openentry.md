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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409616"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。 
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]開くオブジェクトのエントリ識別子へのポインター。
    
 _lpInterface_
  
> [in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合、オブジェクトの標準インターフェイスが返されます。 たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは [IMessage です](imessageimapiprop.md)。フォルダーの場合 [、IMAPIFolder です](imapifolderimapicontainer.md)。 アドレス帳オブジェクトの標準インターフェイスは、 [配布リストの IDistList、](idistlistimapicontainer.md) メッセージング ユーザー [の IMailUser](imailuserimapiprop.md) です。 
    
 _ulOpenFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> 呼び出し元に許可される最大ネットワークアクセス許可を使用してオブジェクトを開く要求。 たとえば、呼び出し元に読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みとして開く必要があります。呼び出し元に読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用として開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> **オブジェクトが呼び出** し元から完全にアクセスできる前に、OpenEntry が正常に返されるのを許可します。 オブジェクトにアクセスできない場合は、後続のオブジェクト呼び出しを実行すると、エラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用として開かれません。呼び出し元は、読み取り/書き込みアクセス許可が付与されているという前提では動作しません。 
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたか、ユーザーが不十分なアクセス許可を持つオブジェクトにアクセスしようとした。
    
MAPI_E_NOT_FOUND 
  
> lpEntryID パラメーターで渡されたエントリ識別子に関連  _付けられたオブジェクトは含_ めではありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID_ パラメーターで渡されるエントリ識別子は、認識できない形式です。 通常、この値は、オブジェクトを含むアドレス帳プロバイダーが開いていない場合に返されます。 
    
## <a name="remarks"></a>注釈

**IMAPISupport::OpenEntry メソッド** は、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは **IMAPISupport::OpenEntry** を呼び出して、特定のオブジェクトにアクセスするために使用できるインターフェイスへのポインターを取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**IMAPISupport::OpenEntry** を呼び出すのは、開いているオブジェクトの種類が分からない場合のみです。 フォルダーまたはメッセージを開いているとわかっている場合は、代わりに [IMsgStore::OpenEntry を](imsgstore-openentry.md) 呼び出します。 アドレス帳コンテナー、メッセージング ユーザー、または配布リストを開いている場合は [、IAddrBook::OpenEntry を呼び出します](iaddrbook-openentry.md)。 これらのより具体的なメソッドは **、IMAPISupport::OpenEntry よりも高速です**。 
  
 **IMAPISupport::OpenEntry** は  _、ulFlags_ パラメーターで MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定し、アクセス許可で十分でない限り、すべてのオブジェクトを読み取り専用として開きます。 これらのフラグのいずれかを設定しても、特定の種類のアクセスが保証されるという保証はありません。付与されるアクセス許可は、アクセス レベル、オブジェクト、およびオブジェクトを所有するサービス プロバイダーによって異なります。 開いたオブジェクトのアクセス レベルを確認するには、そのオブジェクト [(PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md) **PR_ACCESS_LEVELプロパティを** 取得します。
  
_lpulObjType_ パラメーターで返される値を確認して、返されるオブジェクトの種類が予期した値かどうかを確認します。 オブジェクトの種類が想定通りである場合は  _、lppUnk_ パラメーターから適切な型のポインターにポインターをキャストします。 たとえば、フォルダーを開く場合は  _、lppUnk_ を LPMAPIFOLDER 型のポインターにキャストします。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

