---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409231"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナー、メッセージング ユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスを提供します。
  
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
  
> [in]開くコンテナー、メッセージング ユーザー、または配布リストのエントリ識別子へのポインター。
    
 _lpInterface_
  
> [in]開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、オブジェクトの標準インターフェイスの識別子を返します。 コンテナーの場合、標準インターフェイスは [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。 アドレス帳オブジェクトの標準インターフェイスは、配布リストの [IDistList : IMAPIContainer、](idistlistimapicontainer.md) メッセージング ユーザーの [IMailUser : IMAPIProp](imailuserimapiprop.md) です。 
    
 _ulFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセス権を使用してオブジェクトを開く要求。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用のアクセス許可で開く必要があります。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のクライアントがオブジェクトに完全にアクセスする前に **、OpenEntry** メソッドが正常に返されます。 オブジェクトにアクセスしない場合、後続のオブジェクト呼び出しを実行するとエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセス権で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されたと想定する必要があります。
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="remarks"></a>注釈

S_OK 
  
> オブジェクトが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーがオブジェクトを開くアクセス許可が不足しているか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開く試み。
    
MAPI_E_NOT_FOUND 
  
> _lpEntryID で指定されたエントリ識別子は_、オブジェクトを表すではありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID_ パラメーターのエントリ識別子は、アドレス帳プロバイダーによって認識される形式ではありません。 
    
## <a name="remarks"></a>注釈

MAPI は **OpenEntry メソッドを呼** び出して、コンテナー、メッセージング ユーザー、または配布リストを開きます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI が **OpenEntry** メソッドを呼び出す前に  _、lpEntryID_ パラメーターのエントリ識別子がユーザーに属し、別のプロバイダーに属していないと判断します。 MAPI は、エントリ識別子の [MAPIUID](mapiuid.md)構造を、起動時に [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出して登録した **MAPIUID** と照合することでこれを行います。 
  
_ulFlags_ パラメーターで MAPI_MODIFYまたはMAPI_BEST_ACCESSを設定しない限り、オブジェクトを読み取り専用として開きます。 要求されたオブジェクトの変更を許可しない場合は、オブジェクトを一向に開かMAPI_E_NO_ACCESS。 
  
MAPI が  _lpEntryID_ に NULL を渡す場合は、コンテナー階層でルート コンテナーを開きます。
  
開く必要があるオブジェクトは、別のプロバイダーからコピーされたオブジェクトである可能性があります。 この場合、このプロパティは PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートします。 オブジェクトがこのプロパティをサポートしている場合は [、IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーのこのエントリのコードにバインドし _、lpTemplateID_ パラメーターに _PR_TEMPLATEID、ulTemplateFlags_ パラメーターに 0 を渡します。  **IMAPISupport::OpenTemplateID** は、外部プロバイダーの [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) メソッドへの呼び出しで、この情報を外部プロバイダーに渡します。 **IMAPISupport::OpenTemplateID** がエラーを発生する場合は、通常、外部プロバイダーが使用できないか、プロファイルに含まれていないため、非送信エントリを読み取り専用として扱って続行してください。 外部アドレス帳エントリを開く方法の詳細については、「ホスト アドレス帳プロバイダーとして機能する」 [を参照してください](acting-as-a-host-address-book-provider.md)。
  
## <a name="see-also"></a>関連項目



[IABLogon : IUnknown](iablogoniunknown.md)

