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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 53dfb62bb33a4941e2b5627e729763101e24319d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800342"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**適用対象**: Outlook 
  
コンテナー、ユーザー、または配布リストにメッセージを開き、さらにアクセスを提供するインターフェイスの実装にポインターを返します。
  
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
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]メッセージングのユーザー、または配布リストを開き、コンテナーのエントリの識別子へのポインター。
    
 _lpInterface_
  
> [in]開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すことは、オブジェクトの標準的なインタ フェースの識別子を返します。 コンテナーでは、標準のインタ フェースは[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。 標準インターフェイスを使用しているアドレス帳オブジェクト[IDistList: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[IMailUser: IMAPIProp](imailuserimapiprop.md)メッセージング ユーザーのです。 
    
 _ulFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_BEST_ACCESS 
  
> ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を持つオブジェクトを開くことを要求します。 たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用権限を持つオブジェクトを開く必要があります。
    
MAPI_DEFERRED_ERRORS 
  
> **OpenEntry**メソッドが正常に完了、可能性のある呼び出し元のクライアントが完全にオブジェクトを利用する前にすることができます。 オブジェクト アクセスできない場合は、後続のオブジェクトの呼び出しを実行するとエラーが発生します。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用のアクセス権を持つオブジェクトが開いているし、クライアントの読み取り/書き込み権限が付与されていると仮定する必要があります。
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="remarks"></a>注釈

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーには十分なアクセス許可、オブジェクトを開くか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開くしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_で指定されたエントリの識別子は、オブジェクトを表していません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_パラメーターのエントリ id がアドレス帳プロバイダーで認識される形式ではありません。 
    
## <a name="remarks"></a>注釈

MAPI では、ユーザー、または配布リストにメッセージを開くには、コンテナーでは、 **OpenEntry**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

MAPI の**OpenEntry**メソッドを呼び出すと、前にして、別のプロバイダーに、 _lpEntryID_パラメーターのエントリの識別子が属していることを決定します。 MAPI は、メソッドを呼び出して、 [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)の起動時に登録した**MAPIUID**のエントリの識別子では、 [MAPIUID](mapiuid.md)構造を照合することによって行われます。 
  
_UlFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグが設定されていない場合は、読み取り専用としてオブジェクトを開きます。 要求されたオブジェクトの変更を許可しない場合はすべてのオブジェクトを開くされず、MAPI_E_NO_ACCESS を返します。 
  
MAPI では、 _lpEntryID_に NULL が成功した場合は、コンテナー階層のルート コンテナーを開きます。
  
別のプロバイダーからコピーしたオブジェクトを開くにが求められているオブジェクトがあります。 この例では、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートします。 オブジェクトはこのプロパティをサポートしている場合は、外部のプロバイダーでは、 _lpTemplateID_パラメーターで 0 _ulTemplateFlags の**PR_TEMPLATEID**を渡すことでこの記事のコードにバインドする[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出す_パラメーター。 **IMAPISupport::OpenTemplateID**は、この情報を外部のプロバイダーの[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドの呼び出しで外部プロバイダーに渡します。 **IMAPISupport::OpenTemplateID**では、エラーが発生した場合は、通常外部プロバイダーが使用できない場合や、プロファイルに含まれていませんので続行しようと読み取り専用で非連結のエントリを処理することによって。 外部アドレス帳のエントリを開く方法の詳細については、[ホストのアドレス帳プロバイダーとしての機能](acting-as-a-host-address-book-provider.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon : IUnknown](iablogoniunknown.md)

