---
title: mapisvc.inf メッセージサービスセクションのリストエントリ
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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>mapisvc.inf メッセージサービスセクションのリストエントリ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セクションリストエントリには2つの種類があります。1つはサービスプロバイダーセクションと、その他のメッセージサービス固有のセクションを一覧にしたものです。 これらの2種類のエントリは、次の形式を使用して mapisvc.inf に表示されます。
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

**Providers**エントリの各セクションは、メッセージサービスに属するサービスプロバイダーの構成情報を提供する個々のセクションにマップされます。 セクションエントリの各**** セクションは、メッセージサービスに必要なその他の構成情報を含むセクションにマッピングされます。 メッセージサービス実装者は、標準セクションに含まれない特別な情報を含める必要がある場合に、追加のセクションを定義します。 通常、複雑な構成のメッセージサービスでは、[**セクション**] エントリを使用して追加情報を追加します。 すべてのメッセージサービスセクションには、リスト内の少なくとも1つのセクションを持つ**プロバイダー**エントリがあります。すべてのメッセージサービスセクションに**セクション**エントリが含まれているわけではありません。 
  
メッセージサービスセクションの2つの例を次に示します。 最初のセクションは、前の図の既定のアドレス帳サービス用であり、単一のサービスプロバイダーを持つ簡単なメッセージサービスです。 2番目のセクションは、2つのサービスプロバイダーを持つより複雑なサンプルメッセージサービスである msgservice サービスを対象としています。 
  
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

**[msgservice]** セクションの**セクション**エントリには、2つの追加セクション ( **[First_Special_Section]** と、もう1つは **[Second_Special_Section])** が表示されます。 その他のセクションに表示されるデータは、特定のメッセージサービスにとって意味があります。 これらのセクションは次のように表示され、その他のセクションを示しています。 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


