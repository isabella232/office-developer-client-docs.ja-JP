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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="01542-103">mapisvc.inf メッセージサービスセクションのリストエントリ</span><span class="sxs-lookup"><span data-stu-id="01542-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="01542-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01542-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01542-105">セクションリストエントリには2つの種類があります。1つはサービスプロバイダーセクションと、その他のメッセージサービス固有のセクションを一覧にしたものです。</span><span class="sxs-lookup"><span data-stu-id="01542-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="01542-106">これらの2種類のエントリは、次の形式を使用して mapisvc.inf に表示されます。</span><span class="sxs-lookup"><span data-stu-id="01542-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="01542-107">**Providers**エントリの各セクションは、メッセージサービスに属するサービスプロバイダーの構成情報を提供する個々のセクションにマップされます。</span><span class="sxs-lookup"><span data-stu-id="01542-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="01542-108">セクションエントリの各\*\*\*\* セクションは、メッセージサービスに必要なその他の構成情報を含むセクションにマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="01542-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="01542-109">メッセージサービス実装者は、標準セクションに含まれない特別な情報を含める必要がある場合に、追加のセクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="01542-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="01542-110">通常、複雑な構成のメッセージサービスでは、[**セクション**] エントリを使用して追加情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="01542-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="01542-111">すべてのメッセージサービスセクションには、リスト内の少なくとも1つのセクションを持つ**プロバイダー**エントリがあります。すべてのメッセージサービスセクションに**セクション**エントリが含まれているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="01542-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="01542-112">メッセージサービスセクションの2つの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="01542-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="01542-113">最初のセクションは、前の図の既定のアドレス帳サービス用であり、単一のサービスプロバイダーを持つ簡単なメッセージサービスです。</span><span class="sxs-lookup"><span data-stu-id="01542-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="01542-114">2番目のセクションは、2つのサービスプロバイダーを持つより複雑なサンプルメッセージサービスである msgservice サービスを対象としています。</span><span class="sxs-lookup"><span data-stu-id="01542-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="01542-115">**[msgservice]** セクションの**セクション**エントリには、2つの追加セクション ( **[First_Special_Section]** と、もう1つは **[Second_Special_Section])** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01542-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="01542-116">その他のセクションに表示されるデータは、特定のメッセージサービスにとって意味があります。</span><span class="sxs-lookup"><span data-stu-id="01542-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="01542-117">これらのセクションは次のように表示され、その他のセクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="01542-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


