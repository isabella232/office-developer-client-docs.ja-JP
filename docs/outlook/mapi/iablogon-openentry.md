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
  
コンテナー、メッセージングユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスできるようにします。
  
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
  
> 順番開くコンテナー、メッセージングユーザー、または配布リストのエントリ識別子へのポインター。
    
 _lpinterface_
  
> 順番開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスの識別子が返されます。 コンテナーの場合、標準インターフェイスは[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)です。 アドレス帳オブジェクトの標準インターフェイスは[idistlist: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[idistlist: imapiprop](imailuserimapiprop.md)がメッセージングユーザーを対象としています。 
    
 _ulFlags_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに対して許可される最大のネットワークアクセス許可と、クライアントアプリケーションの最大アクセス権を使用して、オブジェクトを開くように要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合、そのオブジェクトは読み取り専用アクセス許可で開かれている必要があります。
    
MAPI_DEFERRED_ERRORS 
  
> **openentry**メソッドを正常に返すことができるようにします。これは、呼び出し元クライアントが完全にオブジェクトにアクセスする前である可能性があります。 オブジェクトがアクセスされていない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセスで開かれ、クライアントは読み取り/書き込みアクセス許可が与えられていると想定することはできません。
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="remarks"></a>注釈

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーがオブジェクトを開くための十分な権限を持っていないか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開こうとしました。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_で指定されたエントリ識別子は、オブジェクトを表していません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_パラメーターのエントリ id は、アドレス帳プロバイダーで認識される形式ではありません。 
    
## <a name="remarks"></a>注釈

MAPI は**openentry**メソッドを呼び出して、コンテナー、メッセージングユーザー、または配布リストを開きます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI は、 **openentry**メソッドを呼び出す前に、 _lpentryid_パラメーターのエントリ識別子が自分に属していること、および別のプロバイダーには属していないことを判断します。 MAPI では、エントリ識別子の[MAPIUID](mapiuid.md)構造を、起動時に[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出すことによって登録した**MAPIUID**と照合することによって、これを行います。 
  
_ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグが設定されていない場合は、オブジェクトを読み取り専用として開きます。 要求されたオブジェクトの変更が許可されていない場合は、オブジェクトを開かずに MAPI_E_NO_ACCESS を返します。 
  
MAPI が_lな tryid_に対して NULL を渡す場合は、コンテナー階層のルートコンテナーを開きます。
  
開くように求められているオブジェクトは、別のプロバイダーからコピーされたオブジェクトである可能性があります。 この場合は、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートします。 オブジェクトがこのプロパティをサポートしている場合は、 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーのこのエントリのコードにバインドし、 _lpTemplateID_パラメーターで**PR_TEMPLATEID**を渡し、ultemplateflags では0にします。 __ パラメーター。 **imapisupport:: OpenTemplateID**は、外部プロバイダーの[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドへの呼び出しで、この情報を外部プロバイダーに渡します。 **imapisupport:: OpenTemplateID**がエラーを発生させる場合は、通常、外部プロバイダーが使用できないか、プロファイルに含まれていないため、非連結エントリを読み取り専用として処理することによって処理を続行します。 外部アドレス帳エントリを開く方法の詳細については、「[ホストアドレス帳プロバイダーとして機能する](acting-as-a-host-address-book-provider.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon : IUnknown](iablogoniunknown.md)

