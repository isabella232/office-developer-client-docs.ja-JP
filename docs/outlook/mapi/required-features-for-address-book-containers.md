---
title: アドレス帳コンテナーの必須機能
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
# <a name="required-features-for-address-book-containers"></a>アドレス帳コンテナーの必須機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ほとんどのアドレス帳プロバイダーは、少なくとも1つのコンテナーをサポートしています。一部は変更可能です。 アドレス帳コンテナーは、コンテンツおよび階層テーブル、検索機能、および名前解決を提供できます。 変更可能なコンテナーを使用すると、メッセージングユーザー、配布リスト、その他のコンテナーなどのエントリを削除したり、他のコンテナー内のエントリや1回限りのテンプレートからエントリを追加したりできます。
  
次の表では、コンテナー、変更可能または読み取り専用、およびそれらの実装方法に関して、アドレス帳プロバイダーに必要な機能について説明します。
  
|**機能**|**実装方法**|
|:-----|:-----|
|メッセージングユーザーにアクセスする  <br/> |[IABLogon:: openentry](iablogon-openentry.md)メソッドを実装します。 詳細については、「[アドレス帳エントリを開く](opening-address-book-entries.md)」を参照してください。  <br/> |
|メッセージングユーザーを比較する  <br/> |[IABLogon:: compareentryids](iablogon-compareentryids.md)メソッドを実装します。 詳細については、「[アドレス帳エントリの比較](comparing-address-book-entries.md)」を参照してください。  <br/> |
|メッセージングユーザーを作成する  <br/> |1. **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティをサポートすることによって、1回限りのテーブルに作成テンプレートのリストを指定します。 詳細については、「 [1 つのコンテナーの1回限りのテーブルの実装](implementing-a-container-one-off-table.md)」を参照してください。  <br/> 2. [IABContainer:: createentry](iabcontainer-createentry.md)メソッドを実装します。 詳細については、「[アドレス帳のエントリを追加する](adding-address-book-entries.md)」を参照してください。  <br/> |
|メッセージングユーザーのコピー  <br/> |[IABContainer:: copyentries](iabcontainer-copyentries.md)メソッドを実装します。 詳細については、「[アドレス帳エントリのコピー](copying-address-book-entries.md)」を参照してください。  <br/> |
|メッセージングユーザーを削除する  <br/> |[IABContainer::D eleteentries](iabcontainer-deleteentries.md)メソッドを実装します。 詳細については、「[アドレス帳のエントリを削除](removing-address-book-entries.md)する」を参照してください。  <br/> |
|メッセージングユーザーに関する概要情報を提供する  <br/> |container プロパティの**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) をサポートします。 詳細については、「 [Contents Tables](contents-tables.md)」を参照してください。  <br/> |
|メッセージングユーザーに関する詳細情報を提供する  <br/> |メッセージングユーザーおよび配布リストに対して**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートします。 詳細については、「[受信者情報の表示](displaying-recipient-information.md)と[表の表示](display-tables.md)」を参照してください。  <br/> |
|コンテナーに関する詳細情報を提供する  <br/> |コンテナーで**PR_DETAILS_TABLE**プロパティをサポートします。 詳細については、「[受信者情報の表示](displaying-recipient-information.md)と[表の表示](display-tables.md)」を参照してください。  <br/> |
|コンテナーの階層リストを提供する  <br/> |container プロパティの**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) をサポートします。 詳細については、「[階層テーブル](hierarchy-tables.md)」を参照してください。  <br/> |
|メッセージングユーザープロパティのサポート  <br/> |[imailuser: imapiprop](imailuserimapiprop.md)インターフェイスを実装します。  <br/> |
|あいまいな名前の解決  <br/> | **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限をサポートします。  <br/>  必要に応じて、 [IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを実装します。 For more information, see [Implementing Name Resolution](implementing-name-resolution.md).  <br/> |
   

