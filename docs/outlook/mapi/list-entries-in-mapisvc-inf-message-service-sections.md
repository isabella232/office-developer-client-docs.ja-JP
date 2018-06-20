---
title: MapiSvc.inf のメッセージ サービスのセクションで、リストのエントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cfb06e8dd305add6049d035c44685be047dc744f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801271"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>MapiSvc.inf のメッセージ サービスのセクションで、リストのエントリ

  
  
**適用されます**: Outlook 
  
セクションのリストのエントリの 2 種類があります: サービス プロバイダー セクションおよびその他のメッセージ サービスに固有のセクションを一覧表示する一覧を表示します。 Mapisvc.inf の以下のファイル形式でこれらの 2 種類のエントリが表示されます。
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

**プロバイダー**エントリ内の各セクションは、メッセージ サービスが属するサービス ・ プロバイダーの構成情報を提供する個々 のセクションにマップされます。 **セクション**エントリ内の各セクションは、メッセージ サービスで必要となる余分な構成情報を含むセクションにマップされます。 メッセージ サービスの実装者は、標準のセクションに適合しない特殊な情報が含まれている場合、余分なセクションを定義します。 複雑な構成通常メッセージ サービスでは、余分な情報を追加するのに**セクション**のエントリを使用します。 メッセージ サービスのすべてのセクションには、**プロバイダー**のエントリのリストに少なくとも 1 つのセクションでメッセージ サービスのすべてのセクションでは、**セクション**のエントリがあります。 
  
メッセージ サービスのセクションの 2 つの例に従います。 最初のセクションでは、図では、1 つのサービス プロバイダーの簡単なメッセージ サービスからアドレス帳の既定のサービスのこと。 2 番目のセクションは、MsgService サービスは、次の 3 つのサービス プロバイダーとのより複雑なサンプル メッセージ サービスです。 
  
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

**[MsgService]** セクションの**セクション**のエントリの一覧の他の 2 つのセクション、1 つと呼ばれる **[First_Special_Section]** と **[Second_Special_Section]** と呼ばれる別のです。 余分なセクション内に表示されるデータは、特定のメッセージ サービスに有効です。 これらのセクションには、余分なセクションを説明するために次の情報が表示されます。 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


