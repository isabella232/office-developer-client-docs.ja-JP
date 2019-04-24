---
title: アドレス帳プロバイダーの必須機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328694"
---
# <a name="required-features-for-address-book-providers"></a>アドレス帳プロバイダーの必須機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは、一時または恒久、ローカルまたはリモートの、1つまたは複数のメッセージングシステムによって認識され、ディスクファイルまたはデータベーステーブル用にフォーマットされた受信者情報を処理できます。 アドレス帳プロバイダーが実装できるさまざまな機能があり、それにより、クライアントやその他のプロバイダーとの相互運用性が向上します。 ただし、いくつかの機能が必要です。
  
次の表では、すべてのアドレス帳プロバイダーに必要な機能と、それらを実装するために必要な手順について説明します。
  
|**機能**|**実装方法**|
|:-----|:-----|
|セッションログオン  <br/> | エントリポイント関数を実装します。 詳細については、「[アドレス帳プロバイダーエントリポイント関数の実装](implementing-an-address-book-provider-entry-point-function.md)」を参照してください。  <br/>  [IABProvider:: Logon](iabprovider-logon.md)メソッドを実装します。 詳細については、「[アドレス帳プロバイダーのログオンとログオフの実装](implementing-address-book-provider-logon-and-logoff.md)」を参照してください。  <br/> |
|セッションログオフ  <br/> |[IABProvider:: Shutdown](iabprovider-shutdown.md)メソッドを実装します。 詳細については、「[アドレス帳プロバイダーのログオンとログオフの実装](implementing-address-book-provider-logon-and-logoff.md)」を参照してください。  <br/> |
|エントリ識別子を作成する  <br/> |**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティのサポートを提供します。 詳細については、「 [MAPI エントリ識別子](mapi-entry-identifiers.md)と[アドレス帳識別子](address-book-identifiers.md)」を参照してください。  <br/> |
|状態テーブルに投稿する  <br/> | [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスの適切なメソッドを実装します。 詳細については、「 [Status オブジェクトの実装](status-object-implementation.md)」を参照してください。  <br/>  必要な状態テーブルのプロパティをサポートします。 詳細については、「 [Status Tables](status-tables.md)」を参照してください。  <br/>  Call [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)。  <br/> |
|限定的な状態オブジェクトのサポートを提供する  <br/> | [imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを実装します。  <br/>  他の**imapistatus**メソッドから MAPI_E_NO_SUPPORT を返します。  <br/> |
|対話型およびプログラムによる構成のサポート  <br/> | メッセージサービスエントリポイント関数を実装します。  <br/>  表示テーブルを実装します。 詳細については、「表と[表示テーブルの実装](display-table-implementation.md)を[表示](display-tables.md)する」を参照してください。  <br/>  プロパティシートを実装するか、 [imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出します。 詳細については、「[プロパティシートの実装](property-sheet-implementation.md)」を参照してください。  <br/> |
   
また、プロバイダーが受信者の作成をサポートしている場合は、作成テンプレートの一覧を指定する必要があります。 この一覧を提供するには、 [IABLogon:: getoneofftable](iablogon-getoneofftable.md)メソッドを実装して、プロバイダーがサポートするすべてのテンプレートと、各コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを使用して、 **PR_CREATE_TEMPLATES** [を開きます。PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティと、コンテナーでサポートされているすべてのテンプレートを含みます。 詳細については、「 [1 回限りのテーブルの実装](implementing-one-off-tables.md)」を参照してください。
  

