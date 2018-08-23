---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 619357a608dd160cbe4811cc7db7ae3b392db858
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576891"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダーまたはメッセージのオブジェクトを開くし、さらにアクセスを提供するオブジェクトへのポインターを返します。 
  
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
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。 
    
 _lpEntryID_
  
> [in]フォルダーまたはメッセージを開くにはオブジェクトのエントリ id のアドレスへのポインター。 
    
 _lpInterface_
  
> [in]オブジェクトのインターフェイス id (IID) へのポインター。 NULL を渡すには、このようなオブジェクトの標準的なインタ フェースにオブジェクトをキャストすることを示します。 _LpInterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子を設定することも。 
    
 _ulOpenFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_BEST_ACCESS 
  
> ユーザーと最大のクライアント アプリケーションのアクセス許可で許可される最大のアクセス許可を持つオブジェクトを開く必要があります。 たとえば、クライアントに読み取り/書き込み権限がある場合は、オブジェクトを開くと読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用権限を持つオブジェクトが開かれます。 クライアントは、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得することによって、アクセス許可レベルを取得できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出しは、基になるオブジェクトが呼び出し元のアプリケーションに利用可能でない場合でも、成功するために許可されています。 オブジェクトが使用できない場合は、オブジェクトへの後続の呼び出しはエラーを返すことがあります。
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用の権限を持つオブジェクトが作成され、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

MAPI は、メッセージ ストア内のフォルダーまたはメッセージを開くに**IMSLogon::OpenEntry**メソッドを呼び出します。 MAPI を開くにはオブジェクトのエントリ id を渡します。 メッセージ ストア プロバイダーは、 _lppUnk_パラメーターで指定したオブジェクトにさらにアクセスできるようにするためのポインターを返す必要があります。 
  
MAPI では、 **IMSLogon::OpenEntry**を呼び出し、前に、最初に指定したメッセージまたはフォルダーのエントリ id と一致しているこのメッセージ ストア プロバイダーが登録されているいずれかを決定します。 エントリの識別子では、ストア プロバイダーを登録する方法の詳細については[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を参照してください。
  
 **IMSLogon::OpenEntry**は、メッセージ ストアのオブジェクトの[IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドをクライアントに**IMSLogon::OpenEntry**は呼び出しませんMAPI は、 **IMAPISession::OpenEntry**メソッドを処理するときに**IMSLogon::OpenEntry**を呼び出します。 オブジェクトの**IMSLogon::OpenEntry**を使用して開く必要がありますメッセージを使用して開かれたオブジェクトの格納オブジェクトとまったく同じに扱われます具体的には、この呼び出しを使用して開かれたオブジェクトは、メッセージ ストア オブジェクトを離したとき無効にするべき。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

