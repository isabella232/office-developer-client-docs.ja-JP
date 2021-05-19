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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409336"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーまたはメッセージを開き、さらにアクセスするインターフェイス ポインターを返します。 
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト 数  _です。_
    
 _lpEntryID_
  
> [in]開くオブジェクトのエントリ識別子 (NULL) へのポインター。 _lpEntryID が_ NULL に設定されている場合 **、OpenEntry は** メッセージ ストアのルート フォルダーを開きます。 
    
 _lpInterface_
  
> [in]開いたオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡した場合、オブジェクトの標準インターフェイス ([フォルダーの IMAPIFolder](imapifolderimapicontainer.md) とメッセージの [IMessage)](imessageimapiprop.md) が返されます。 
    
 _ulFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを使用できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセスを使用してオブジェクトを開く要求。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、オブジェクトは読み取り/書き込みアクセス許可を使用して開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用アクセス許可を使用して開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> オブジェクトが呼び出し元のクライアントで完全に利用できる前に **、OpenEntry** が正常に返されるのを許可します。 オブジェクトを使用できない場合は、後続のオブジェクト呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で開き、クライアントは読み取り/書き込みアクセス許可が付与されるという前提で動作しません。 
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたり、ユーザーのアクセス許可が不十分なオブジェクトにアクセスしようとしたりしました。
    
MAPI_NO_CACHE
  
> キャッシュ モードでストアを開いた場合、クライアントまたはサービス プロバイダーは **IMsgStore::OpenEntry** を呼び出し、MAPI_NO_CACHE フラグを設定してリモート ストア上のアイテムまたはフォルダーを開きます。 リモート サーバーで MDB_ONLINE フラグを指定してメッセージ ストアを開く場合は、メッセージ ストア フラグをMAPI_NO_CACHEする必要があります。
    
## <a name="remarks"></a>注釈

**IMsgStore::OpenEntry** メソッドは、フォルダーまたはメッセージを開き、さらにアクセスするために使用できるインターフェイスへのポインターを返します。 
  
> [!IMPORTANT]
> フォルダーやメッセージなどのパブリック ストアでフォルダー エントリを開く場合は [、IMAPISession::OpenEntry](imapisession-openentry.md)の代わりに **IMsgStore::OpenEntry** を使用します。 これにより、複数のアカウントがプロファイルで定義されている場合Exchangeパブリック フォルダーが正しく機能します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_ulFlags_ パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定しない限り、フォルダーとメッセージは読み取り専用のアクセス許可で自動的に開きます。 これらのフラグのいずれかを設定しても、特定の種類のアクセス許可は保証されない。付与されるアクセス許可は、メッセージ ストア プロバイダー、アクセス レベル、およびオブジェクトによって異なります。 開いたオブジェクトのアクセス レベルを確認するには、そのオブジェクト [(PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md) **PR_ACCESS_LEVELプロパティを** 取得します。
  
**IMsgStore::OpenEntry** を使用して任意のフォルダーまたはメッセージを開く場合は、通常 [、IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを使用する方が、開くフォルダーまたはメッセージの親フォルダーにアクセスできる方が高速です。 
  
_lpulObjType_ パラメーターで返される値を確認して、返されるオブジェクトの種類が予期した値であるかどうかを確認します。 オブジェクトの種類が予期しない型の場合は  _、lppUnk_ パラメーターから適切な型のポインターにポインターをキャストします。 たとえば、フォルダーを開く場合は  _、lppUnk_ を **LPMAPIFOLDER** 型のポインターにキャストします。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI は **、IMsgStore::OpenEntry** メソッドを使用して、エントリ ID に関連付けられたオブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

