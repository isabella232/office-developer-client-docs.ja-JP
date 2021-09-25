---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 103feb1641f9537b0f521c0bfd6696879603f852
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567418"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
外部アドレス帳プロバイダーで受信者エントリを開きます。
  
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
  
> [in]  _lpTemplateID_ が指すテンプレート識別子のバイト数です。 
    
 _lpTemplateID_
  
> [in]開く受信者エントリの **テンプレート** PR_TEMPLATEID ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。
    
 _ulTemplateFlags_
  
> [in]エントリを開く方法を説明するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
FILL_ENTRY 
  
> 新しいエントリが作成されています。 外部プロバイダーは、後続の [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) 呼び出しを MAPI から受信すると  _、lpMAPIPropData_ パラメーターが指すプロパティを変更するか  _、lppMAPIPropNew_ で特定のインターフェイス実装を返して、新しいエントリのプロパティを設定する方法を制御することで、エントリの作成方法を制御できます。 
    
 _lpMAPIPropData_
  
> [in]呼び出し元がエントリへのアクセスに使用するインターフェイス実装へのポインター。 これは、外部プロバイダーが独自の実装でラップし  _、lppMAPIPropNew_ パラメーターに戻す実装です。 _lpMAPIPropData_ パラメーターは [、IMAPIProp : IUnknown](imapipropiunknown.md)から派生し _、lpInterface_ パラメーターで要求されるインターフェイスをサポートする読み取り/書き込みインターフェイス実装を指している必要があります。 
    
 _lpInterface_
  
> [in]エントリへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lppMAPIPropNew_ パラメーターは _、lpInterface_ で指定された型のインターフェイスをポイントします。 NULL を渡すと、メッセージング ユーザーの標準インターフェイスが返IID_IMailUser。 
    
 _lppMAPIPropNew_
  
> [out]外部プロバイダーがエントリにアクセスするために提供するインターフェイス実装へのポインター。
    
 _lpMAPIPropSibling_
  
> 予約済み。NULL である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> バインド プロセスが成功しました。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> 外部アドレス帳プロバイダーが存在しません。
    
## <a name="remarks"></a>注釈

**IMAPISupport::OpenTemplateID** メソッドは、アドレス帳プロバイダーのサポート オブジェクトにのみ実装されます。 **OpenTemplateID** は、他のアドレス帳プロバイダー (外部プロバイダーとも呼ばれる) に属するエントリのホストとして機能できるアドレス帳プロバイダーによってのみ呼び出されます。 ホスト プロバイダーは **OpenTemplateID** を呼び出して外部エントリを開きます。これは、ホスト プロバイダーのデータが外部プロバイダーのコードにバインドされている場合に発生します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**OpenTemplateID を呼** び出すのは、外部アドレス帳プロバイダーからのテンプレート識別子を持つエントリの格納をサポートしている場合のみです。 このようなサポートは [、IABContainer::CreateEntry](iabcontainer-createentry.md) および [IABLogon::OpenEntry 実装](iablogon-openentry.md) に追加の要件を設定します。 詳細については、これらのメソッドの説明とホスト アドレス帳プロバイダーとしての機能を [参照してください](acting-as-a-host-address-book-provider.md)。
  
**OpenTemplateID 呼** び出しがバインド インターフェイスとして返される場合は、渡したのと同じプロパティ オブジェクト実装を使用して、プロパティ オブジェクトへの参照を解放できます。 これは、外部プロバイダーが独自の参照を保持するためにオブジェクトの **AddRef** メソッドを呼び出したためです。 外部プロバイダーがプロパティ オブジェクトへの参照を保持する必要が無い場合 **、OpenTemplateID** はアンバウンド プロパティ オブジェクトを返します。 
  
**OpenTemplateID に** エラーがMAPI_E_UNKNOWN_ENTRYID場合は、エントリを読み取り専用として扱って続行してください。 
  
## <a name="see-also"></a>関連項目



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid 標準プロパティ](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

