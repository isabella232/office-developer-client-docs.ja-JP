---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a120fb1710bf2bd351d956e4d05eb0af346ef4c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583387"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ホストのアドレス帳プロバイダーに存在するデータが含まれている受信者のエントリが表示されます。
  
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
  
> [in]_LpTemplateID_パラメーターで指定されたテンプレートの識別子のバイト数です。 
    
 _lpTemplateID_
  
> [in]テンプレート識別子、または受信者のエントリを開くことの**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティへのポインター。
    
 _ulTemplateFlags_
  
> [in]テンプレート識別子によって表される項目を開く方法を指定するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
FILL_ENTRY 
  
> テンプレート識別子によって表される項目に基づいて、コンテナーでホスト プロバイダーに新しいエントリを作成しています。 **IABLogon::OpenTemplateID**メソッドを使用してホスト プロバイダーのエントリの特定の初期化を実行する必要がありますか、 [IMAPIProp: IUnknown](imapipropiunknown.md) _lpMAPIPropData_のパラメーターまたは戻り値のカスタム**IMAPIProp の実装**インターフェイスの実装は、 _lppMAPIPropNew_パラメーターにします。 
    
 _lpMAPIPropData_
  
> [in]**IMAPIProp**から派生したホスト プロバイダーのプロパティのオブジェクトとインターフェイスの実装へのポインター。
    
 _lpInterface_
  
> [in]_LppMAPIPropNew_パラメーターで返されるインターフェイス ポインターの型を表すインターフェイス識別子 (IID) へのポインター。 標準のユーザー インターフェイスのメッセージを返します**null**を渡す[IMailUser: IMAPIProp](imailuserimapiprop.md)。
    
 _lppMAPIPropNew_
  
> [out]**IMAPIProp**から派生したプロパティがバインドされているオブジェクトとインターフェイスの実装へのポインター。
    
 _lpMAPIPropSibling_
  
> [out]予約されています。**null**にする必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 適切なコードは、ホスト プロバイダーに関連するデータを正常にバインドされました。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、テンプレートの Id をサポートしていません。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> アドレス帳プロバイダーでは、 _lpTemplateID_パラメーターに渡されるテンプレート識別子は認識されません。 
    
## <a name="remarks"></a>注釈

**IABLogon::OpenTemplateID**メソッドは、ホスト プロバイダーのコンテナー内にあるそれぞれのエントリのコピーの制御を維持する必要のあるアドレス帳プロバイダーによってのみ実装されます。 **OpenTemplateID**を実装するプロバイダーは、外部のアドレス帳プロバイダーと呼ばれます。 ホスト プロバイダーがコピーしたエントリを作成またはコピーした項目を開くには、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出すし、MAPI は、 **IABLogon::OpenTemplateID**の呼び出しに渡されます。 **IABLogon::OpenTemplateID**は、エントリを表示し、ホスト プロバイダー内のデータにそれを制御するコードをバインドします。 
  
エントリ id を使用するのではなく、 **IABLogon::OpenTemplateID**は、エントリのテンプレートの識別子、 **PR_TEMPLATEID**、別のプロパティを使用します。 テンプレート識別子は、ホスト プロバイダーでのデータにバインドする必要がありますコードを持つエントリをサポートする必要があります。
  
いくつかのアドレス帳プロバイダーが**IABLogon::OpenTemplateID**を実装する場合の例は次のとおり。 
  
- そのままとするためにコピーしたエントリのデータを定期的に更新するには、元と同期されます。
    
- 機能を実装する動的にサーバー上のデータからのエントリの詳細の表に表示される一覧の作成など、ホスト プロバイダーを実装できません。
    
- ホスト プロバイダーのエントリのプロパティと、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) を含む別の詳細表示の編集コントロールの値からの計算など、元のエントリとの間の対話を制御するにはアドレスのコンポーネントです。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

ホスト プロバイダーにコピーまたは、プロバイダーからのエントリを作成し、 **IABLogon::OpenTemplateID**を通じてプロパティ オブジェクトの実装を指定する、ほとんどのエントリを維持するために呼び出しを処理します。 ただし、ホスト プロバイダーにこれらの呼び出しを転送するため、ホスト プロバイダーの呼び出しを傍受でき、呼び出しを転送する前にカスタム処理を実行します。
  
プロパティのオブジェクトの実装では、次のガイドラインを使用してください。
  
- [IMAPIProp::GetProps](imapiprop-getprops.md)が呼び出されると場合は、処理と計算されたプロパティは、要求するかどうかを決定します。 ホスト プロバイダーには、メジャーのプロパティに対するすべての要求を転送します。 
    
- 開くには[IMAPIProp::OpenProperty](imapiprop-openproperty.md)が呼び出されたときに詳細を除く任意のテーブルはテーブルを表示する、要求を処理します。 ほとんどのテーブルは、ホスト プロバイダーに正確にコピーできません。 **IMAPITable**実装これらの要求されたテーブルを生成する必要があります。 ホスト プロバイダーに詳細テーブルの**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティをコピーする必要があります。 これにより、ローカルにテーブルを生成するには、このプロバイダーです。 表示テーブルの通知を生成するテーブルの表示の実装をラップすることもできます。 
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)が呼び出されると、ホスト プロバイダーは、プロパティを設定するを許可する前にデータを検証できます。 すべての必要なプロパティが設定された計算を確認することができます。 エラーが検出された場合は、適切なエラー値を返すと、可能なら、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)で、追加の説明です。
    
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出されると、ホスト プロバイダーすることも、エントリを保存する前に、処理を実行します。 ホスト プロバイダーのエントリで、新しいアドレスなど、変更されたプロパティの影響を受けるすべてのデータを保存する必要があります。 
    
一般に、ホスト プロバイダーに渡されたエントリの実装を行うすべての関連するプロパティのコンテキストに固有の操作を実行するメソッドをインターセプトします。 FILL_ENTRY フラグが_ulTemplateFlags_パラメーターで渡された場合は、エントリのすべてのプロパティを設定します。 
  
_LppMAPIPropNew_パラメーターで新しい property オブジェクトを取得する場合は、参照を維持するために、ホスト プロバイダーのプロパティのオブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。 **IMAPIProp**実装は、 _lppMAPIPropNew_で返されるバインドされたオブジェクトをすべての呼び出しをルーティングするプロパティのホスト オブジェクトのそれぞれの対応するメソッドにバインドされたオブジェクトによって処理される、後。 
  
バインドされたプロパティ オブジェクトを通じて渡される任意の名前付きプロパティのプロパティ id は、プロバイダーの識別子の名前空間には。 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドの実装は、任意のテンプレートに固有のタスクを実行できるようにするプロパティの名前を判断します。 同様に、ホスト プロバイダーに渡す、プロバイダーのプロパティは、名前空間である必要があります。 などの**OpenTemplateID**では、名前付きプロパティを設定する場合必要がありますを使用する、識別子の 1 つの名前- [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出すことによって、必要に応じて、作成します。 
  
_LpTemplateID_に渡されたエントリ id を認識していない場合は、MAPI_E_UNKNOWN_ENTRYID を返します。
  
アドレス帳テンプレートの識別子を操作する方法の詳細については、[外部のアドレス帳プロバイダーとしての機能](acting-as-a-foreign-address-book-provider.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid 標準プロパティ](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

