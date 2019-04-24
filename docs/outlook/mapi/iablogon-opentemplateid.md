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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334749"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ホストアドレス帳プロバイダーに存在するデータを持つ受信者エントリを開きます。
  
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
  
> 順番_lpTemplateID_パラメーターによって指定されるテンプレート識別子のバイト数。 
    
 _lpTemplateID_
  
> 順番開く受信者エントリのテンプレート識別子または**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。
    
 _ultemplateflags_
  
> 順番テンプレート識別子で表されるエントリを開く方法を示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
FILL_ENTRY 
  
> ホストプロバイダーは、テンプレート識別子によって表されるエントリに基づいて、コンテナー内に新しいエントリを作成しています。 **IABLogon:: OpenTemplateID**メソッドは、 _lpMAPIPropData_パラメーターの[imapiprop: IUnknown](imapipropiunknown.md)実装を使用してホストプロバイダーのエントリの特定の初期化を実行するか、カスタム imapiprop を返す必要があります。 **** _lppMAPIPropNew_パラメーターでのインターフェイスの実装。 
    
 _lpMAPIPropData_
  
> 順番ホストプロバイダーの property オブジェクトへのポインターと、 **imapiprop**から派生したインターフェイスの実装。
    
 _lpinterface_
  
> 順番_lppMAPIPropNew_パラメーターで返されるインターフェイスポインターの種類を表すインターフェイス識別子 (IID) へのポインター。 **null**を渡すと、標準のメッセージングユーザーインターフェイス、 [imailuser: imapiprop](imailuserimapiprop.md)が返されます。
    
 _lppMAPIPropNew_
  
> 読み上げバインドされた property オブジェクトへのポインターと、 **imapiprop**から派生したインターフェイスの実装。
    
 _lpMAPIPropSibling_
  
> 読み上げ予約語**null**である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 適切なコードがホストプロバイダーの関連データに正常にバインドされました。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトはテンプレート id をサポートしていません。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpTemplateID_パラメーターで渡されたテンプレート識別子がアドレス帳プロバイダーで認識されません。 
    
## <a name="remarks"></a>解説

**IABLogon:: OpenTemplateID**メソッドは、ホストプロバイダーのコンテナーにあるエントリのコピーに対する制御を維持する必要があるアドレス帳プロバイダーによってのみ実装されます。 **OpenTemplateID**を実装するプロバイダーは、外部アドレス帳プロバイダーと呼ばれます。 ホストプロバイダーは[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)を呼び出してコピーされたエントリを作成するか、コピーされたエントリを開くと、 **IABLogon:: OpenTemplateID**の呼び出しに MAPI が渡されます。 **IABLogon:: OpenTemplateID**はエントリを開き、ホストプロバイダーのデータに制御するコードをバインドします。 
  
**IABLogon:: OpenTemplateID**は、エントリ識別子を使用するのではなく、別のプロパティ、エントリのテンプレート識別子、 **PR_TEMPLATEID**を使用します。 ホストプロバイダーのデータにコードをバインドする必要があるエントリに対して、テンプレート識別子をサポートする必要があります。
  
アドレス帳プロバイダーが**IABLogon:: OpenTemplateID**を実装する必要がある場合の例としては、次のようなものがあります。 
  
- コピーしたエントリのデータを定期的に更新して、元のデータと同期されたままにします。
    
- サーバー上のデータからエントリの詳細表に表示されるリストを動的に設定するなど、ホストプロバイダーが実装できない機能を実装します。
    
- ホストプロバイダーのエントリ内のプロパティと元の項目の間の相互作用を制御するには、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) を、異なる詳細表示にある編集コントロールの値を使用して計算します。住所のコンポーネント。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

ホストプロバイダーは、プロバイダーからエントリをコピーまたは作成するときに、 **IABLogon:: OpenTemplateID**を使用してプロパティオブジェクトの実装を提供するときに、エントリを維持するために、ほとんどの呼び出しを処理します。 ただし、ホストプロバイダーは、このような呼び出しを自分に転送する必要があるので、呼び出しを転送する前に、ホストプロバイダーは任意の呼び出しを受信し、カスタム処理を実行できます。
  
property オブジェクトの実装では、次のガイドラインを使用する必要があります。
  
- [imapiprop:: GetProps](imapiprop-getprops.md)が呼び出されたときに、要求が計算されたプロパティを対象としているかどうかを判別し、ある場合は処理します。 非計算プロパティのすべての要求をホストプロバイダーに転送します。 
    
- [imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出して、詳細表示テーブル以外の任意のテーブルを開いた場合は、要求を処理します。 ほとんどのテーブルは、ホストプロバイダに正確にコピーすることはできません。 これらの要求されたテーブルに対して**IMAPITable**実装を生成する必要があります。 詳細表**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをホストプロバイダーにコピーする必要があります。 これにより、このプロバイダーはテーブルをローカルに生成できるようになります。 表示テーブルの通知を生成するために、表示テーブルの実装をラップする必要がある場合があります。 
    
- [imapiprop:: setprops](imapiprop-setprops.md)が呼び出されると、ホストプロバイダーはプロパティを設定する前にデータを検証することができます。 必要なすべてのプロパティが設定または計算されたことを確認できます。 エラーが検出された場合は、適切なエラー値を返します。可能であれば、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)から追加の説明を返します。
    
- [imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出されると、ホストプロバイダーはエントリを保存する前に処理を実行することができます。 新しいアドレスなど、変更されたプロパティの影響を受けるすべてのデータを、ホストプロバイダのエントリに保存する必要があります。 
    
一般的には、ホストプロバイダーに渡すエントリの実装によって、関連するプロパティのコンテキスト固有の操作を実行するすべてのメソッドがインターセプトされます。 FILL_ENTRY フラグが_ultemplateflags_パラメーターに渡された場合は、エントリのすべてのプロパティを設定します。 
  
_lppMAPIPropNew_パラメーターで新しい property オブジェクトを取得する場合は、ホストプロバイダーの property オブジェクトの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して、参照を維持します。 _lppMAPIPropNew_での**imapiprop**の実装によって返されたバインドオブジェクトを経由するすべての呼び出しは、バインドされたオブジェクトによって処理された後、host property オブジェクトの対応するメソッドにルーティングされる必要があります。 
  
バインドされた property オブジェクトを通じて渡される名前付きプロパティのプロパティ識別子は、プロバイダーの識別子名前空間にあります。 [imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドを実装すると、テンプレート固有のタスクを実行できるように、プロパティの名前を決定する必要があります。 同様に、プロバイダーがホストプロバイダーに渡すプロパティも、名前空間に存在する必要があります。 たとえば、 **OpenTemplateID**で名前付きプロパティを設定する場合は、必要に応じて、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出すことによって、その名前に識別子の1つを使用する必要があります。 
  
_lpTemplateID_で渡されたエントリ識別子を認識しない場合は、MAPI_E_UNKNOWN_ENTRYID を返します。
  
アドレス帳テンプレート識別子を操作する方法の詳細については、「[外部アドレス帳プロバイダーとして機能](acting-as-a-foreign-address-book-provider.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid 標準プロパティ](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

