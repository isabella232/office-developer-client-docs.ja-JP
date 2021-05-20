---
title: アドレス帳コンテナーに必要な機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439682"
---
# <a name="required-features-for-address-book-containers"></a>アドレス帳コンテナーに必要な機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ほとんどのアドレス帳プロバイダーは、少なくとも 1 つのコンテナーをサポートします。一部のコンテナーは変更可能です。 アドレス帳コンテナーは、コンテンツテーブルと階層テーブル、検索機能、および名前解決を提供できます。 変更可能なコンテナーを使用すると、メッセージング ユーザー、配布リスト、その他のコンテナーなどのエントリを削除し、他のコンテナーまたは 1 回限りテンプレートのエントリからエントリを追加できます。
  
次の表では、コンテナー、変更可能または読み取り専用のアドレス帳プロバイダーに必要な機能と、それらを実装する方法について説明します。
  
|**機能**|**実装方法**|
|:-----|:-----|
|メッセージング ユーザーにアクセスする  <br/> |[IABLogon::OpenEntry メソッドを実装](iablogon-openentry.md)します。 詳細については、「アドレス帳エントリ [を開く」を参照してください](opening-address-book-entries.md)。  <br/> |
|メッセージング ユーザーの比較  <br/> |[IABLogon::CompareEntryIDs メソッドを実装](iablogon-compareentryids.md)します。 詳細については、「アドレス帳 [エントリの比較」を参照してください](comparing-address-book-entries.md)。  <br/> |
|メッセージング ユーザーの作成  <br/> |1. プロパティ ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティをサポートして、1 **回PR_CREATE_TEMPLATES** 作成テンプレートの一覧を指定します。 詳細については、「Container [One-Offテーブルの実装」を参照してください](implementing-a-container-one-off-table.md)。  <br/> 2. [IABContainer::CreateEntry メソッドを実装](iabcontainer-createentry.md) します。 詳細については、「アドレス帳エントリ [の追加」を参照してください](adding-address-book-entries.md)。  <br/> |
|メッセージング ユーザーのコピー  <br/> |[IABContainer::CopyEntries メソッドを実装](iabcontainer-copyentries.md)します。 詳細については [、「Copying Address Book Entries」を参照してください](copying-address-book-entries.md)。  <br/> |
|メッセージング ユーザーの削除  <br/> |[IABContainer::D eleteEntries メソッドを実装](iabcontainer-deleteentries.md)します。 詳細については、「アドレス帳 [エントリの削除」を参照してください](removing-address-book-entries.md)。  <br/> |
|メッセージング ユーザーに関する概要情報を提供する  <br/> |コンテナー プロパティを **サポートPR_CONTAINER_CONTENTS** [(PidTagContainerContents)。](pidtagcontainercontents-canonical-property.md) 詳細については、「コンテンツ テーブル [」を参照してください](contents-tables.md)。  <br/> |
|メッセージング ユーザーに関する詳細情報を提供する  <br/> |メッセージング ユーザー **PR_DETAILS_TABLE** 配布リストで [、プロパティ (PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)プロパティをサポートします。 詳細については、「受信者情報の [表示」および「テーブルの表示](displaying-recipient-information.md) 」 [を参照してください](display-tables.md)。  <br/> |
|コンテナーに関する詳細情報を提供する  <br/> |コンテナーの **PR_DETAILS_TABLE** プロパティをサポートします。 詳細については、「受信者情報の [表示」および「テーブルの表示](displaying-recipient-information.md) 」 [を参照してください](display-tables.md)。  <br/> |
|コンテナーの階層リストを提供する  <br/> |コンテナー プロパティを **サポートPR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)。](pidtagcontainerhierarchy-canonical-property.md) 詳細については、「階層テーブル [」を参照してください](hierarchy-tables.md)。  <br/> |
|メッセージング ユーザーのプロパティをサポートする  <br/> |[IMailUser : IMAPIProp インターフェイスを実装](imailuserimapiprop.md)します。  <br/> |
|あいまいな名前を解決する  <br/> | プロパティの **制限** PR_ANR ([PidTagAnr](pidtaganr-canonical-property.md)) をサポートします。  <br/>  必要に応じて [、IABContainer::ResolveNames メソッドを実装](iabcontainer-resolvenames.md) します。 For more information, see [Implementing Name Resolution](implementing-name-resolution.md).  <br/> |
   

