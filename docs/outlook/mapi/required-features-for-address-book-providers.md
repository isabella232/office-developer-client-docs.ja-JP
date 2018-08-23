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
ms.openlocfilehash: ac76d1caf5db0b041a17d40d08671665b5427051
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803750"
---
# <a name="required-features-for-address-book-providers"></a>アドレス帳プロバイダーの必須機能

  
  
**適用対象**: Outlook 
  
アドレス帳プロバイダーは、一時的または永続的なローカルまたはリモート、1 つまたは複数のメッセージング システムで認識されています、ディスク ファイルまたはデータベース テーブルの書式設定された受信者の情報を操作できます。 さまざまな値を追加して、クライアントおよびその他のプロバイダーとの相互運用性を向上させるために、アドレス帳プロバイダーが実装できる機能があります。 ただし、いくつかの機能は、必要があります。
  
次の表は、すべてのアドレス帳プロバイダーが必要な機能とそれを実装するために必要な手順について説明します。
  
|**機能**|**実装する方法**|
|:-----|:-----|
|セッション ログオン  <br/> | エントリ ポイント関数を実装します。 詳細については、[アドレス帳プロバイダーのエントリ ポイント関数を実装する](implementing-an-address-book-provider-entry-point-function.md)を参照してください。  <br/>  [IABProvider::Logon](iabprovider-logon.md)メソッドを実装します。 詳細については、[実装するアドレス帳プロバイダーへのログオンとログオフ](implementing-address-book-provider-logon-and-logoff.md)を参照してください。  <br/> |
|セッションのログオフ  <br/> |[IABProvider::Shutdown](iabprovider-shutdown.md)メソッドを実装します。 詳細については、[実装するアドレス帳プロバイダーへのログオンとログオフ](implementing-address-book-provider-logon-and-logoff.md)を参照してください。  <br/> |
|エントリの識別子を作成します。  <br/> |**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティのサポートを提供します。 詳細については、 [MAPI のエントリの識別子](mapi-entry-identifiers.md)と[アドレス帳の識別子](address-book-identifiers.md)を参照してください。  <br/> |
|ステータス テーブルに投稿します。  <br/> | 適切なメソッドを実装、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。 詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。  <br/>  必要な状態テーブルのプロパティをサポートします。 詳細については、[ステータス ・ テーブル](status-tables.md)を参照してください。  <br/>  [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出します。  <br/> |
|限られた状態のオブジェクトのサポートを提供します。  <br/> | [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを実装します。  <br/>  **IMAPIStatus**の他のメソッドから MAPI_E_NO_SUPPORT を返します。  <br/> |
|インタラクティブおよびプログラマティックなの構成をサポート  <br/> | メッセージ サービスのエントリ ポイント関数を実装します。  <br/>  表示テーブルを実装します。 詳細については、[テーブルを表示](display-tables.md)し、[表示テーブルの実装](display-table-implementation.md)を参照してください。  <br/>  プロパティ シートを実装または[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出します。 詳細については、[プロパティ シートの実装](property-sheet-implementation.md)を参照してください。  <br/> |
   
さらに、プロバイダーは、受信者の作成をサポートする場合は、作成テンプレートの一覧を指定してください。 すべてのプロバイダーとを開くには、 **PR_CREATE_TEMPLATES** ([ 、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)のメソッドの各コンテナーでサポートされているテンプレートを含むように[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを実装することによりこのリストを提供します。PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティのコンテナーでサポートされているすべてのテンプレートが含まれるとします。 詳細については、[一時テーブルを実装する](implementing-one-off-tables.md)を参照してください。
  

