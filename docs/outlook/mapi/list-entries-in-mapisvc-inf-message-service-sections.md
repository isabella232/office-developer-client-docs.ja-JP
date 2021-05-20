---
title: MapiSvc.inf メッセージ サービス セクションのエントリの一覧
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435930"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>MapiSvc.inf メッセージ サービス セクションのエントリの一覧

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セクション リスト エントリには、サービス プロバイダー セクションを一覧表示するエントリと、その他のメッセージ サービス固有のセクションを一覧表示する 2 種類があります。 これらの 2 種類のエントリは、次の形式を使用して mapisvc.inf に表示されます。
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Providers エントリの **各セクション** は、メッセージ サービスに属するサービス プロバイダーの構成情報を提供する個別のセクションにマップされます。 セクション エントリの **各セクション** は、メッセージ サービスに必要な追加の構成情報を含むセクションにマップされます。 メッセージ サービスの実装者は、標準セクションに収まらない特別な情報を含める場合に、追加のセクションを定義します。 複雑な構成を持つメッセージ サービスでは、通常 **、Sections** エントリを使用して、追加の情報を追加します。 すべてのメッセージ サービス セクションには、リストに **少** なくとも 1 つのセクションを含む Providers エントリがあります。一部のメッセージ サービス セクションに **Sections エントリが含されていない** 場合。 
  
メッセージ サービス セクションの 2 つの例を次に示します。 最初のセクションは、前の図の既定のアドレス帳サービス用で、単一のサービス プロバイダーを持つ簡単なメッセージ サービスです。 2 番目のセクションは、3 つのサービス プロバイダーを持つ、より複雑なサンプル メッセージ サービスである MsgService サービスです。 
  
```cpp
[AB]
PR_DISPLAY_NAME=Default Address Book
Providers=AB Provider
PR_SERVICE_DLL_NAME=AB.DLL
PR_SERVICE_SUPPORT_FILES=AB.DLL
PR_SERVICE_ENTRY_NAME=DABServiceEntry
PR_RESOURCE_FLAGS=SERVICE_NO_PRIMARY_IDENTITY
[MsgService]
PR_DISPLAY_NAME=My Own Service
Providers=MsgService Prov1, MsgService Prov2, MsgService Prov3
Sections=First_Special_Section, Second_Special_Section
PR_SERVICE_DLL_NAME=MYSERV.DLL
PR_SERVICE_SUPPORT_FILES=MYSERV.DLL, MYXXX.DLL, MYZZZ.DLL
PR_SERVICE_ENTRY_NAME=MyServiceEntry
PR_RESOURCE_FLAGS=SERVICE_SINGLE_COPY
66040003=00000000

```

**[MsgService]** セクションの **Sections** エントリには、[First_Special_Section] と呼ばれるセクションと **[Second_Special_Section]** という 2 **つのセクションが一覧表示されます**。 余分なセクションに表示される可能性のあるデータは、特定のメッセージ サービスにとって意味があります。 これらのセクションは、追加のセクションを示す次のように表示されます。 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


