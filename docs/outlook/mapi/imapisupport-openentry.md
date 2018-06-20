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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 04bf7f2ddda7377df72417df2472246a2cf329bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800780"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**適用されます**: Outlook 
  
オブジェクトを開き、さらにアクセスするためのインターフェイス ポインターを返します。 
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはオブジェクトのエントリの識別子へのポインター。
    
 _lpInterface_
  
> [in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 パラメーターに NULL が返されるオブジェクトの標準的なインタ フェースで発生します。 などのオブジェクトを開くことができませんが、メッセージの場合は、標準のインタ フェースは、 [IMessage](imessageimapiprop.md)です。フォルダー、 [IMAPIFolder](imapifolderimapicontainer.md)です。 アドレス帳オブジェクトの標準的なインターフェイスは、配布リストおよび[IMailUser](imailuserimapiprop.md)のメッセージング ユーザーの[IDistList](idistlistimapicontainer.md)です。 
    
 _ulOpenFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_BEST_ACCESS 
  
> 呼び出し元で使用できる最大のネットワーク アクセス許可を持つオブジェクトを開くことを要求します。 たとえば、呼び出し元に読み取り/書き込み権限がある場合は、オブジェクトで開いてください読み取り/書き込み。呼び出し元に読み取り専用のアクセス許可が設定されている場合は、読み取り専用で、オブジェクトを開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> **OpenEntry**を正常に完了、可能性のあるオブジェクトが呼び出し元に完全にアクセス可能にするを使用できます。 オブジェクトがアクセスできない場合は、後続のオブジェクトの呼び出しを行うことができますと、エラーです。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、オブジェクトが読み取り専用で開いているし、呼び出し元は読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしましたまたは、ユーザーが十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_パラメーターで渡されたエントリの識別子に関連付けられているオブジェクトではありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_パラメーターで渡されたエントリ id が、認識できない形式です。 この値は通常、オブジェクトが含まれるアドレス帳プロバイダーが開いていない場合に返されます。 
    
## <a name="remarks"></a>備考

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::OpenEntry**メソッドを実装します。 サービス プロバイダーは、特定のオブジェクトへのアクセスに使用できるインターフェイスへのポインターを取得するために**IMAPISupport::OpenEntry**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

開いているオブジェクトの種類がわからない場合にのみ、 **IMAPISupport::OpenEntry**を呼び出します。 フォルダーまたはメッセージを開くことがわかっている場合は、代わりに[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 アドレス帳コンテナーである、メッセージング ユーザー、または配布リストを開くことがわかっている場合は、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 これらの具体的な方法は、 **IMAPISupport::OpenEntry**よりも高速です。 
  
 _UlFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグを設定して、アクセス許可が十分でない限り、 **IMAPISupport::OpenEntry**は読み取り専用で、すべてのオブジェクトを開きます。 これらのフラグのいずれかを設定では特定の種類のアクセスは保証されません。付与されたアクセス許可は、ユーザーのアクセス レベル、オブジェクト、およびオブジェクトを所有しているサービス プロバイダーによって異なります。 開かれたオブジェクトのアクセス レベルを決定するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得します。
  
返されるオブジェクトの種類では何が必要と判断するのには_lpulObjType_パラメーターで返される値を確認してください。 オブジェクトの型が予期したとおりの場合は、 _lppUnk_パラメーターの適切な型のポインターへのポインターにキャストします。 などのフォルダーを開いている場合は、LPMAPIFOLDER の型のポインターに_lppUnk_をキャストします。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

