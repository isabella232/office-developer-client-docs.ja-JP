---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f087e5fd301ade7331a3681be6042ec61b48493c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596450"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ホスト アドレス帳プロバイダーに存在するデータを含む受信者エントリを開きます。
  
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
  
> [in]  _lpTemplateID_ パラメーターが指すテンプレート識別子のバイト 数。 
    
 _lpTemplateID_
  
> [in]開く受信者エントリのテンプレート **識別子または** PR_TEMPLATEID ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。
    
 _ulTemplateFlags_
  
> [in]テンプレート識別子で表されるエントリを開く方法を示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
FILL_ENTRY 
  
> ホスト プロバイダーは、テンプレート識別子で表されるエントリに基づいて、コンテナー内に新しいエントリを作成しています。 **IABLogon::OpenTemplateID** メソッドは [、imapIProp : iUnknown](imapipropiunknown.md)実装を _lpMAPIPropData_ パラメーターで使用してホスト プロバイダーのエントリの特定の初期化を実行するか _、lppMAPIPropNew_ パラメーターでカスタム **IMAPIProp** インターフェイス実装を返す必要があります。 
    
 _lpMAPIPropData_
  
> [in]ホスト プロバイダーのプロパティ オブジェクトへのポインターと **IMAPIProp** から派生したインターフェイスの実装。
    
 _lpInterface_
  
> [in]  _lppMAPIPropNew_ パラメーターで返されるインターフェイス ポインターの種類を表すインターフェイス識別子 (IID) へのポインター。 **null を渡** すと、標準のメッセージング ユーザー インターフェイス [IMailUser : IMAPIProp が返されます](imailuserimapiprop.md)。
    
 _lppMAPIPropNew_
  
> [out]バインドされたプロパティ オブジェクトへのポインターと **IMAPIProp** から派生したインターフェイスの実装。
    
 _lpMAPIPropSibling_
  
> [out]予約済み。null である **必要があります**。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 適切なコードがホスト プロバイダーの関連データに正常にバインドされました。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトはテンプレートの ID をサポートしていない。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpTemplateID_ パラメーターで渡されたテンプレート識別子は、アドレス帳プロバイダーによって認識されません。 
    
## <a name="remarks"></a>注釈

**IABLogon::OpenTemplateID** メソッドは、ホスト プロバイダーのコンテナーにあるエントリのコピーを管理する必要があるアドレス帳プロバイダーによってのみ実装されます。 **OpenTemplateID を実装するプロバイダー** は、外部アドレス帳プロバイダーと呼ばれる。 ホスト プロバイダーは [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) を呼び出してコピーされたエントリを作成するか、コピーしたエントリを開き、MAPI は **IABLogon::OpenTemplateID** に呼び出しを渡します。 **IABLogon::OpenTemplateID は** エントリを開き、それを制御するコードをホスト プロバイダーのデータにバインドします。 
  
**IABLogon::OpenTemplateID** は、エントリ識別子を使用するのではなく、別のプロパティ (エントリのテンプレート識別子) を使用 **PR_TEMPLATEID。** ホスト プロバイダーのデータにコードをバインドする必要があるエントリでは、テンプレート識別子をサポートする必要があります。
  
アドレス帳プロバイダーが **IABLogon::OpenTemplateID** を実装する必要がある場合の例を次に示します。 
  
- コピーしたエントリのデータを定期的に更新して、元のエントリと同期を維持するには。
    
- サーバー上のデータからエントリの詳細テーブルに表示されるリストを動的に設定するなど、ホスト プロバイダーが実装できない機能を実装する。
    
- アドレスの異なるコンポーネントを含む詳細表示の編集コントロールの値から **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の計算など、ホスト プロバイダーのエントリのプロパティと元のエントリの間の相互作用を制御します。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

ホスト プロバイダーがプロバイダーからエントリをコピーまたは作成し **、IABLogon::OpenTemplateID** を使用してプロパティ オブジェクトの実装を指定すると、ほとんどの呼び出しを処理してエントリを維持します。 ただし、ホスト プロバイダーがこれらの呼び出しを転送する必要がある場合、ホスト プロバイダーは任意の呼び出しを傍受し、呼び出しを転送する前にカスタム処理を実行できます。
  
プロパティ オブジェクトの実装では、次のガイドラインを使用する必要があります。
  
- [IMAPIProp::GetProps](imapiprop-getprops.md)が呼び出された場合は、要求が計算されたプロパティ用であるかどうかを判断し、その場合は処理します。 非計算プロパティのすべての要求をホスト プロバイダーに転送します。 
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)が呼び出され、詳細表示テーブル以外のテーブルを開く場合は、要求を処理します。 ほとんどのテーブルをホスト プロバイダーに正確にコピーすることはできません。 これらの要求されたテーブルに **対して IMAPITable** 実装を生成する必要があります。 プロパティの詳細 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをホスト プロバイダーにコピーする必要があります。 これにより、このプロバイダーはテーブルをローカルで生成できます。 表示テーブルの実装をラップして、表示テーブル通知を生成する場合があります。 
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)が呼び出された場合、ホスト プロバイダーは、プロパティを設定する前にデータを検証できます。 必要なすべてのプロパティが設定または計算されたと確認できます。 エラーが検出された場合は、適切なエラー値を返し、可能な場合は [IMAPIProp::GetLastError](imapiprop-getlasterror.md)を使用して追加の説明を返します。
    
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出された場合、ホスト プロバイダーは、エントリを保存する前に処理を実行する必要があります。 変更されたプロパティ (新しいアドレスなど) の影響を受けるデータは、ホスト プロバイダーのエントリに保存する必要があります。 
    
一般に、ホスト プロバイダーに返すエントリの実装を、関連するプロパティのコンテキスト固有の操作を実行するために、すべてのメソッドをインターセプトします。 _ulTemplateFlags_ パラメーター FILL_ENTRYフラグが渡される場合は、エントリのすべてのプロパティを設定します。 
  
_lppMAPIPropNew_ パラメーターで新しいプロパティ オブジェクトを返す場合は、ホスト プロバイダーのプロパティ オブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して参照を維持します。 _lppMAPIPropNew_ で **返された IMAPIProp** 実装がバインドされたオブジェクトを介してのすべての呼び出しは、バインドされたオブジェクトによって処理された後、ホスト プロパティ オブジェクト内の対応するメソッドにルーティングする必要があります。 
  
バインドされたプロパティ オブジェクトを介して渡される名前付きプロパティのプロパティ識別子は、プロバイダーの識別子名前空間にあります。 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドの実装では、テンプレート固有のタスクを実行できるよう、プロパティの名前を決定する必要があります。 同様に、プロバイダーがホスト プロバイダーに渡すプロパティも名前空間に含む必要があります。 **たとえば、OpenTemplateID** で名前付きプロパティを設定する場合は [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出して、名前の識別子の 1 つを使用する必要があります。必要に応じて作成します。 
  
_lpTemplateID_ で渡されたエントリ識別子が認識されない場合は、MAPI_E_UNKNOWN_ENTRYID。
  
アドレス帳テンプレート識別子を使用する方法の詳細については、「外部アドレス帳プロバイダーとして機能する [」を参照してください](acting-as-a-foreign-address-book-provider.md)。
  
## <a name="see-also"></a>関連項目



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid 標準プロパティ](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

