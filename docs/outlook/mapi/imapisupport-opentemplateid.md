---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800785"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**適用されます**: Outlook 
  
外部のアドレス帳で受信者のエントリが表示されます。
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parameters

 _cbTemplateID_
  
> [in]_LpTemplateID_で示されるテンプレート識別子のバイト数です。 
    
 _lpTemplateID_
  
> [in]テンプレート識別子を開くには、受信者のエントリの**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティへのポインター。
    
 _ulTemplateFlags_
  
> [in]エントリを開く方法について説明するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
FILL_ENTRY 
  
> 新しいエントリを作成しています。 _LpMAPIPropData_パラメーターによって、または特定のインターフェイスを返すことによって示されるプロパティを変更することにより、エントリを作成する方法が制御できる外部のプロバイダーでは、MAPI から[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)の後続の呼び出しを受信したとき新しいエントリのプロパティを設定する方法を制御するのには_lppMAPIPropNew_で実装します。 
    
 _lpMAPIPropData_
  
> [in]エントリにアクセスするのには、呼び出し元を使用するインターフェイスの実装へのポインター。 これは、外部のプロバイダーは独自の実装をラップし、 _lppMAPIPropNew_パラメーターに返すの実装です。 _LpMAPIPropData_パラメーターは、読み取り/書き込みインタ フェースの実装から派生する] をポイントする必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 _lpInterface_パラメーターで要求されたインターフェイスをサポートしているとします。 
    
 _lpInterface_
  
> [in]エントリにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _LppMAPIPropNew_パラメーターは、 _lpInterface_によって指定された型のインターフェイスを指します。 NULL を渡すことは、IID_IMailUser、メッセージング ユーザーのための標準インターフェイスを返します。 
    
 _lppMAPIPropNew_
  
> [out]エントリにアクセスするため、外部のプロバイダーが提供するインターフェイスの実装へのポインター。
    
 _lpMAPIPropSibling_
  
> 予約されています。NULL である必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> バインド処理が正常に完了しました。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> 外部のアドレス帳プロバイダーが存在しません。
    
## <a name="remarks"></a>備考

**IMAPISupport::OpenTemplateID**メソッドは、アドレス帳プロバイダーのサポートのオブジェクトに対してのみ実装されます。 **OpenTemplateID**は、他のアドレス帳プロバイダーとも呼ばれる外部プロバイダーに属しているエントリのホストとして機能する、アドレス帳プロバイダーによってのみ呼び出されます。 ホスト プロバイダーは、ホスト プロバイダー内のデータが外部のプロバイダーのコードにバインドされている場合に発生する、外部のエントリを開くには、 **OpenTemplateID**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

外部のアドレス帳プロバイダーからのテンプレートの識別子を持つエントリの保存をサポートする場合にのみ、 **OpenTemplateID**を呼び出します。 このようなサポートは、 [IABContainer::CreateEntry](iabcontainer-createentry.md)と[IABLogon::OpenEntry](iablogon-openentry.md)の実装に追加の要件を配置します。 詳細については、これらのメソッドと[ホストのアドレス帳プロバイダーとしての機能](acting-as-a-host-address-book-provider.md)の説明を参照してください。
  
渡された同じプロパティ オブジェクトの実装、バインドされたインターフェイスと**OpenTemplateID**の呼び出しが返された場合、オブジェクトへの参照、プロパティをリリースできます。 外部プロバイダーが独自の参照を保持するオブジェクトの**AddRef**メソッドを呼び出すためにです。 外部プロバイダーがプロパティ オブジェクトへの参照を保持する必要がない場合**OpenTemplateID**は、プロパティがバインドされていないオブジェクトを返します。 
  
**OpenTemplateID**では、MAPI_E_UNKNOWN_ENTRYID が失敗した場合、読み取り専用で、エントリを処理することで継続してみてください。 
  
## <a name="see-also"></a>関連項目



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid の標準的なプロパティ](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

