---
title: アドレス帳コンテナーの必要な機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5eeaa9a8c1965954ad2eb0a6bfd2a174a355f10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803767"
---
# <a name="required-features-for-address-book-containers"></a>アドレス帳コンテナーの必要な機能

  
  
**適用されます**: Outlook 
  
ほとんどのアドレス帳プロバイダーが少なくとも 1 つのコンテナーがあり、それらの変更の一部をサポートします。 内容と階層構造のテーブル、検索機能、および名前解決、アドレス帳コンテナーを指定できます。 変更可能なコンテナーは、ユーザー、配布リスト、またはその他のコンテナーおよび 1 回限りのテンプレートからその他のコンテナー内のエントリからエントリの追加のメッセージングなどのエントリの削除を使用します。
  
次の表は、アドレス帳プロバイダーを編集可能または読み取り専用のコンテナーを持つに必要な機能を説明し、それらを実装する方法です。
  
|**機能**|**実装する方法**|
|:-----|:-----|
|メッセージング ユーザーをアクセスします。  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md)メソッドを実装します。 詳細については、[開始アドレス帳のエントリ](opening-address-book-entries.md)を参照してください。  <br/> |
|メッセージングのユーザーを比較します。  <br/> |[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)メソッドを実装します。 詳細については、[アドレス帳のエントリを比較する](comparing-address-book-entries.md)を参照してください。  <br/> |
|メッセージングのユーザーを作成します。  <br/> |1. **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティをサポートすることによって一時テーブルの作成テンプレートの一覧を提供します。 詳細については、[コンテナーの一時テーブルを実装する](implementing-a-container-one-off-table.md)を参照してください。  <br/> 2. [IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドを実装します。 詳細については、[アドレス帳のエントリを追加する](adding-address-book-entries.md)を参照してください。  <br/> |
|メッセージング ユーザーをコピーします。  <br/> |[IABContainer::CopyEntries](iabcontainer-copyentries.md)メソッドを実装します。 詳細については、[アドレス帳のエントリのコピー](copying-address-book-entries.md)を参照してください。  <br/> |
|メッセージングのユーザーを削除します。  <br/> |[IABContainer::DeleteEntries](iabcontainer-deleteentries.md)メソッドを実装します。 詳細については、[アドレス帳のエントリを削除する](removing-address-book-entries.md)を参照してください。  <br/> |
|メッセージング ユーザーについての概要情報を提供します。  <br/> |**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のコンテナーのプロパティをサポートします。 詳細については、[内容のテーブル](contents-tables.md)を参照してください。  <br/> |
|メッセージング ユーザーに関する詳細情報を提供します。  <br/> |ユーザーおよび配布リストをメッセージに**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートしてください。 詳細については、[受信者の情報を表示して](displaying-recipient-information.md)[表示のテーブル](display-tables.md)を参照してください。  <br/> |
|コンテナーに関する詳細情報を提供します。  <br/> |コンテナーの**PR_DETAILS_TABLE**プロパティをサポートしてください。 詳細については、[受信者の情報を表示して](displaying-recipient-information.md)[表示のテーブル](display-tables.md)を参照してください。  <br/> |
|コンテナーの階層リストを提供します。  <br/> |**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) のコンテナーのプロパティをサポートします。 詳細については、[階層テーブル](hierarchy-tables.md)を参照してください。  <br/> |
|メッセージング ユーザーのプロパティをサポートします。  <br/> |実装、 [IMailUser: IMAPIProp](imailuserimapiprop.md)インタ フェースです。  <br/> |
|あいまいな名前を解決するには  <br/> | **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) のプロパティの制限をサポートしてください。  <br/>  必要に応じて[IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを実装します。 詳細については、[名前解決の実装](implementing-name-resolution.md)を参照してください。  <br/> |
   

