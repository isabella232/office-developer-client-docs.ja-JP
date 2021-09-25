---
title: アドレス帳プロバイダーに必要な機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ef6075ec05a7272d2657544d5ea89ca5a04d1e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578789"
---
# <a name="required-features-for-address-book-providers"></a>アドレス帳プロバイダーに必要な機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは、一時的または永続的な、ローカルまたはリモートの受信者情報を操作し、1 つ以上のメッセージング システムで理解し、ディスク ファイルまたはデータベース テーブル用に書式設定できます。 アドレス帳プロバイダーが実装できるさまざまな機能があります。これにより、クライアントや他のプロバイダーとの相互運用性を向上させ、価値を高め、相互運用性を向上できます。 ただし、いくつかの機能が必要です。
  
次の表では、すべてのアドレス帳プロバイダーに必要な機能と、それらを実装するために必要な手順について説明します。
  
|**機能**|**実装方法**|
|:-----|:-----|
|セッション ログオン  <br/> | エントリ ポイント関数を実装します。 詳細については、「アドレス帳 [プロバイダーエントリ ポイント関数の実装」を参照してください](implementing-an-address-book-provider-entry-point-function.md)。  <br/>  [IABProvider::Logon メソッドを実装](iabprovider-logon.md)します。 詳細については、「アドレス帳プロバイダー [のログオンとログオフの実装」を参照してください](implementing-address-book-provider-logon-and-logoff.md)。  <br/> |
|セッション ログオフ  <br/> |[IABProvider::Shutdown メソッドを実装](iabprovider-shutdown.md)します。 詳細については、「アドレス帳プロバイダー [のログオンとログオフの実装」を参照してください](implementing-address-book-provider-logon-and-logoff.md)。  <br/> |
|エントリ識別子の作成  <br/> |プロパティ ([PidTagEntryId](pidtagentryid-canonical-property.md) **)** PR_ENTRYIDサポートを提供します。 詳細については [、「MAPI エントリ識別子と](mapi-entry-identifiers.md) アドレス [帳識別子」を参照してください](address-book-identifiers.md)。  <br/> |
|状態テーブルに投稿する  <br/> | [IMAPIStatus : IMAPIProp インターフェイスの適切なメソッドを実装](imapistatusimapiprop.md)します。 詳細については [、「Status Object Implementation」を参照してください](status-object-implementation.md)。  <br/>  必要な状態テーブルのプロパティをサポートします。 詳細については、「Status [Tables」を参照してください](status-tables.md)。  <br/>  [IMAPISupport::ModifyStatusRow を呼び出します](imapisupport-modifystatusrow.md)。  <br/> |
|制限付き状態オブジェクトのサポートを提供する  <br/> | [IMAPIStatus::ValidateState メソッドを実装](imapistatus-validatestate.md)します。  <br/>  他MAPI_E_NO_SUPPORT **IMAPIStatus メソッドから値を** 返します。  <br/> |
|対話型およびプログラムによる構成をサポートする  <br/> | メッセージ サービスエントリ ポイント関数を実装します。  <br/>  表示テーブルを実装します。 詳細については、「Display [Tables and Display Table](display-tables.md) [Implementation」を参照してください](display-table-implementation.md)。  <br/>  プロパティ シートを実装するか [、IMAPISupport::D oConfigPropsheet メソッドを呼び出](imapisupport-doconfigpropsheet.md) します。 詳細については、「プロパティ シートの [実装」を参照してください](property-sheet-implementation.md)。  <br/> |
   
また、プロバイダーが受信者の作成をサポートしている場合は、作成テンプレートの一覧を指定する必要があります。 [IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを実装して、プロバイダーでサポートされているテンプレートと、各コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを実装して **、PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開き、コンテナーでサポートされているテンプレートを含め、このリストを指定します。 詳細については、「テーブルの実装 [」をOne-Offしてください](implementing-one-off-tables.md)。
  

