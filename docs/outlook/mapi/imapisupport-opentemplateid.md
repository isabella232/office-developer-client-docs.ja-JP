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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418506"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
外部アドレス帳プロバイダーの受信者エントリを開きます。
  
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

## <a name="parameters"></a>パラメーター

 _cbTemplateID_
  
> 順番_lpTemplateID_によって示されるテンプレート識別子のバイト数。 
    
 _lpTemplateID_
  
> 順番開く受信者エントリのテンプレート識別子**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。
    
 _ultemplateflags_
  
> 順番エントリを開く方法を示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
FILL_ENTRY 
  
> 新しいエントリが作成されています。 外部プロバイダーは、MAPI から[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)呼び出しを受け取ると、 _lpMAPIPropData_パラメーターで指定されたプロパティを変更するか、特定のインターフェイスを返すことにより、エントリの作成方法を制御できます。_lppMAPIPropNew_での実装。新しいエントリのプロパティを設定する方法を制御します。 
    
 _lpMAPIPropData_
  
> 順番発信者がエントリにアクセスするために使用するインターフェイスの実装へのポインター。 これは、外部プロバイダーが独自の実装でラップして、 _lppMAPIPropNew_パラメーターで返す実装です。 _lpMAPIPropData_パラメーターは、 [imapiprop: IUnknown](imapipropiunknown.md)から派生した読み取り/書き込みインターフェイスの実装を指している必要があり、 _lpinterface_パラメーターで要求されているインターフェイスをサポートしていなければなりません。 
    
 _lpinterface_
  
> 順番エントリへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lppMAPIPropNew_パラメーターは、 _lpinterface_で指定された型のインターフェイスを指します。 NULL を渡すと、メッセージングユーザー IID_IMailUser の標準インターフェイスが返されます。 
    
 _lppMAPIPropNew_
  
> 読み上げ外部プロバイダーがエントリにアクセスするために提供するインターフェイスの実装へのポインター。
    
 _lpMAPIPropSibling_
  
> 予約語NULL である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> バインドプロセスが正常に完了しました。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> 外部アドレス帳プロバイダーが存在しません。
    
## <a name="remarks"></a>注釈

**imapisupport:: OpenTemplateID**メソッドは、アドレス帳プロバイダーサポートオブジェクトに対してのみ実装されています。 **OpenTemplateID**は、他のアドレス帳プロバイダー (外部プロバイダーとも呼ばれる) に属するエントリに対してホストとして動作するアドレス帳プロバイダーによってのみ呼び出されます。 ホストプロバイダーは、 **OpenTemplateID**を呼び出して外部エントリを開きます。これは、ホストプロバイダーのデータが外部プロバイダーのコードにバインドされるときに発生します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**OpenTemplateID**の呼び出しは、外部アドレス帳プロバイダーからのテンプレート識別子を持つエントリの格納をサポートしている場合にのみ行います。 このようなサポートでは、 [IABContainer:: createentry](iabcontainer-createentry.md)および[IABLogon:: openentry](iablogon-openentry.md)実装に追加の要件があります。 詳細については、これらのメソッドの説明を参照し、[ホストアドレス帳プロバイダーとして機能](acting-as-a-host-address-book-provider.md)します。
  
**OpenTemplateID**呼び出しが、渡されたのと同じ property オブジェクトの実装で、バインドされたインターフェイスとして返される場合は、property オブジェクトへの参照を解放することができます。 これは、外部プロバイダーがオブジェクトの**AddRef**メソッドを呼び出して、独自の参照を保持しているためです。 外部プロバイダーが property オブジェクトへの参照を保持する必要がない場合、 **OpenTemplateID**は、非連結プロパティオブジェクトを返します。 
  
**OpenTemplateID**が MAPI_E_UNKNOWN_ENTRYID で失敗する場合は、エントリを読み取り専用として処理することによって続行します。 
  
## <a name="see-also"></a>関連項目



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid 標準プロパティ](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

