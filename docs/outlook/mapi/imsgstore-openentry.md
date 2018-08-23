---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 124208a3f5c6bb300aca3699a04b15e842c46cd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801023"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**適用対象**: Outlook 
  
フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイス ポインターを返します。 
  
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
  
> [in]_._ _LpEntryID_パラメーターで指定されたエントリの識別子のバイト数
    
 _lpEntryID_
  
> [in]オブジェクトを開く、または NULL のエントリの識別子へのポインター。 _LpEntryID_は、NULL に設定されている場合、 **OpenEntry**は、メッセージ ・ ストアのルート フォルダーを開きます。 
    
 _lpInterface_
  
> [in]開かれているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 オブジェクトの結果をパラメーターに NULL (このフォルダーには[IMAPIFolder](imapifolderimapicontainer.md) ) とメッセージの[IMessage](imessageimapiprop.md)の標準的なインターフェイスが返されるのです。 
    
 _ulFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを使用することができます。
    
MAPI_BEST_ACCESS 
  
> ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を使用して、オブジェクトを開くことを要求します。 たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を使用して、クライアントに読み取り専用のアクセス許可がある場合は、読み取り専用のアクセス許可を使用してオブジェクトを開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> **OpenEntry**を正常に戻す、可能性のあるオブジェクトが呼び出し元のクライアントに完全に利用できる前にするにを使用できます。 オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用の権限を持つオブジェクトが開いているし、クライアントが読み取り/書き込み権限が与えられていることを前提に動作しない必要があります。 
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_ACCESS 
  
> しようとは、読み取り専用オブジェクトを変更するか、ユーザーが十分なアクセス許可を持っているオブジェクトへのアクセスにしました。
    
MAPI_NO_CACHE
  
> ストアをキャッシュ モードで開くときに、クライアントまたはサービス プロバイダーは、 **IMsgStore::OpenEntry**項目、またはリモートのストア上のフォルダーを開くに MAPI_NO_CACHE フラグを設定を呼び出すことができます。 リモート サーバー上で MDB_ONLINE フラグを使用してメッセージ ・ ストアを開く場合、MAPI_NO_CACHE フラグを使用する必要はありません。
    
## <a name="remarks"></a>注釈

**IMsgStore::OpenEntry**メソッドは、フォルダーまたはメッセージを開くし、さらにアクセスするために使用できるインターフェイスへのポインターを返します。 
  
> [!IMPORTANT]
> フォルダーやメッセージなどのパブリック ストア上のフォルダーのエントリを開くときは、 [IMAPISession::OpenEntry](imapisession-openentry.md)の代わりに**IMsgStore::OpenEntry**を使用します。 これにより、そのパブリック フォルダー関数正しく複数の Exchange アカウントは、プロファイルで定義されている場合。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォルダーとメッセージが自動的に開きます読み取り専用のアクセス許可を持つ_ulFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグを設定する場合を除き。 これらのフラグのいずれかを設定した場合、アクセス許可の特定の種類は保証されません。付与されたアクセス許可は、メッセージ ストア プロバイダー、ユーザーのアクセス レベル、およびオブジェクトによって異なります。 開かれたオブジェクトのアクセス レベルを決定するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得します。
  
任意のフォルダーまたはメッセージを開くには、 **IMsgStore::OpenEntry**を使用できますが、方が通常高速フォルダーまたはメッセージを開くことの親フォルダーにアクセスする場合、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを使用します。 
  
返されるオブジェクトの種類は、何が必要かどうかを判断するのには_lpulObjType_パラメーターで返される値を確認してください。 オブジェクトの型が予期された型でない場合は、 _lppUnk_パラメーターの適切な型のポインターへのポインターをキャストします。 などのフォルダーを開いている場合は、 **LPMAPIFOLDER**の型のポインターに_lppUnk_をキャストします。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI では、 **IMsgStore::OpenEntry**メソッドを使用して、エントリ ID に関連付けられているオブジェクトを開く  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

