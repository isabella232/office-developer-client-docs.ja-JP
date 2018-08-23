---
title: 受信者の作成
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c596cb219cb1096f186e616c05b8372fef3b42a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799870"
---
# <a name="creating-a-recipient"></a>受信者の作成

  
  
**適用対象**: Outlook 
  
クライアントは、メッセージのアドレスを指定するとき、および変更可能なアドレス帳コンテナーにエントリを追加するには、受信者を作成します。 MAPI には、受信者を作成するための 3 つの方法が用意されています。
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
メッセージのアドレスを使用する受信者を作成するときは、 **IAddrBook::CreateOneOff**を呼び出します。 **CreateOneOff**は、特定のアドレス タイプのアドレスに関連する 1 回限りの特別な形式のエントリの識別子を作成します。 一時アドレスと一時エントリ id の詳細については、 [1 回限りのアドレス](one-off-addresses.md)と[1 回限りのエントリ Id](one-off-entry-identifiers.md)を参照してください。
  
**IAddrBook::NewEntry**する受信者を作成するときに使用されるいずれかの呼び出しまたはコンテナーに追加するのにはメッセージを送信します。 **NewEntry**は、3 つのエントリの識別子を含むパラメーターのペアを持っています。 これらのパラメーターは次のとおりです。 
  
|**パラメーターの組み合わせ**|**説明**|
|:-----|:-----|
| _cbEidContainer_と_lpEidContainer_ <br/> |新しいエントリの配置先となるコンテナーのエントリの識別子です。  <br/> |
| _cbEidNewEntryTpl_と_lpEidNewEntryTpl_ <br/> |使用して新しいエントリを作成するテンプレートのエントリの識別子です。  <br/> |
| _lpcbEidNewEntry_と_lppEidNewEntry_ <br/> |新しいエントリのエントリの識別子です。  <br/> |
   
送信メッセージの受信者を作成するには、0 と NULL を_lpEidContainer_に_cbEidContainer_を設定します。 **NewEntry**は、1 回限りの形式では、同じ種類の**IAddrBook::CreateOneOff**への呼び出しによって生成された受信者に対応するエントリの識別子を持つ受信者を作成します。 
  
特定のコンテナーに挿入される受信者を作成するには、コンテナーのエントリ id とコンテナーのエントリの識別子のバイト数を_cbEidContainer_に_lpEidContainer_を設定します。 
  
受信者を作成するテンプレートを使用するには、テンプレートを使用し、このエントリの識別子のバイト数のカウントには、 _cbEidNewEntryTpl_のエントリ id に_lpEidNewEntryTpl_を設定します。 ほとんどの変更可能なアドレス帳コンテナーは、特定の種類のエントリを作成するため 1 つまたは複数のテンプレートをサポートします。 一時テンプレートは、通常は、常にではなく、ダイアログ ボックス。 テンプレートに情報を入力するには、型の書式が正しいアドレスを持つ受信者が作成されます。 
  
いずれかからには、テンプレート エントリの識別子を取得します。
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) コンテナーの 1 回限り、テーブルの列として**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) を指定するコンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すことによってアクセスプロパティ タグと、インターフェイス識別子と IID_IMAPITable。 
    
- アドレス帳のプロバイダーの**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) と**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) プロパティは、プロバイダーのユーザー オブジェクトをメッセージのエントリ id を保持し、リスト テンプレートを配布します。 
    
> [!NOTE]
> テンプレート識別子と呼ばれるエントリ id の別の種類の新しい項目テンプレートのエントリの識別子を混同しないでください。 テンプレート識別子がエントリの他のプロバイダーからのコピーを維持するためにプロバイダーによってのみ使用します。クライアントによって使用されていませんし、新しいエントリを作成するのには使用されません。 
  
作成するエントリの種類を決定するユーザーを有効にするには、 _cbEidNewEntryTpl_の 0 と_lpEidNewEntryTpl_の場合は NULL を渡します。 **NewEntry**この問題が発生すると、MAPI の一時テーブルから作成された一般的なダイアログ ボックスが表示されます: すべてのプロファイルの各アドレス帳のプロバイダーでサポートされているテンプレートの階層リストです。 
  
アドレスの種類、決定されていますか、 **NewEntry** 、 _lpEidNewEntryTpl_パラメーターまたは一時テーブルの表示からユーザーが選択範囲の設定、表示テーブルを使用して対応するテンプレートが表示されます。 すべての新しい項目テンプレートは、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートします。 
  
**NewEntry**が作成したエントリのエントリの識別子を返すには、 _lpcbEidNewEntry_および_lppEidNewEntry_パラメーターに有効なアドレスを渡します。 MAPI では、 _lppEidNewEntry_と_lpcbEidNewEntry_が指すアドレスに新しいエントリの識別子のバイト数で指定されたアドレスに新しいエントリの識別子を配置します。
  
受信者を作成し、特定のアドレス帳コンテナー内に保存するに[IABContainer::CreateEntry](iabcontainer-createentry.md)を呼び出します。 変更可能なコンテナーでのみこのメソッドを使用することができます-コンテナーを持つ、AB_MODIFIABLE、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティのセットにフラグを設定します。 不変のコンテナーで、アドレス帳プロバイダーは、このメソッドをサポートしていません。 _LpEntryID_パラメーターで指定した型のエントリを作成するためのテンプレートのエントリの識別子を指定します。 
  
_UlCreateFlags_パラメーターには、必要なチェック、重複したエントリと新しいエントリが既存のものに置き換える必要があるかどうかの種類を指定します。 **CreateEntry**は、プロバイダーによって重複するエントリのチェックのための新しいオブジェクトの作成に失敗した場合、必要ありません、エラーや警告が返されますを参照してください。 これらの条件下では、プロバイダーは、成功コードを返します。 
  
コンテナーで直接作業している場合は、正確にコンテナーを作成するアドレスの型がわかっては、 **IABContainer::CreateEntry**を呼び出すし、適切なテンプレートのエントリの識別子を渡します。 アドレス帳プロバイダーは、いくつかの既定の初期プロパティを設定します。**SetProps**を他のユーザーを設定するのにを呼び出すことができます。 ユーザーが関与することはありません。 
  

