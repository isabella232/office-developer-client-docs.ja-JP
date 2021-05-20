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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="46ec2-103">MapiSvc.inf メッセージ サービス セクションのエントリの一覧</span><span class="sxs-lookup"><span data-stu-id="46ec2-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="46ec2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46ec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46ec2-105">セクション リスト エントリには、サービス プロバイダー セクションを一覧表示するエントリと、その他のメッセージ サービス固有のセクションを一覧表示する 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="46ec2-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="46ec2-106">これらの 2 種類のエントリは、次の形式を使用して mapisvc.inf に表示されます。</span><span class="sxs-lookup"><span data-stu-id="46ec2-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="46ec2-107">Providers エントリの **各セクション** は、メッセージ サービスに属するサービス プロバイダーの構成情報を提供する個別のセクションにマップされます。</span><span class="sxs-lookup"><span data-stu-id="46ec2-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="46ec2-108">セクション エントリの **各セクション** は、メッセージ サービスに必要な追加の構成情報を含むセクションにマップされます。</span><span class="sxs-lookup"><span data-stu-id="46ec2-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="46ec2-109">メッセージ サービスの実装者は、標準セクションに収まらない特別な情報を含める場合に、追加のセクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="46ec2-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="46ec2-110">複雑な構成を持つメッセージ サービスでは、通常 **、Sections** エントリを使用して、追加の情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="46ec2-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="46ec2-111">すべてのメッセージ サービス セクションには、リストに **少** なくとも 1 つのセクションを含む Providers エントリがあります。一部のメッセージ サービス セクションに **Sections エントリが含されていない** 場合。</span><span class="sxs-lookup"><span data-stu-id="46ec2-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="46ec2-112">メッセージ サービス セクションの 2 つの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="46ec2-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="46ec2-113">最初のセクションは、前の図の既定のアドレス帳サービス用で、単一のサービス プロバイダーを持つ簡単なメッセージ サービスです。</span><span class="sxs-lookup"><span data-stu-id="46ec2-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="46ec2-114">2 番目のセクションは、3 つのサービス プロバイダーを持つ、より複雑なサンプル メッセージ サービスである MsgService サービスです。</span><span class="sxs-lookup"><span data-stu-id="46ec2-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="46ec2-115">**[MsgService]** セクションの **Sections** エントリには、[First_Special_Section] と呼ばれるセクションと **[Second_Special_Section]** という 2 **つのセクションが一覧表示されます**。</span><span class="sxs-lookup"><span data-stu-id="46ec2-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="46ec2-116">余分なセクションに表示される可能性のあるデータは、特定のメッセージ サービスにとって意味があります。</span><span class="sxs-lookup"><span data-stu-id="46ec2-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="46ec2-117">これらのセクションは、追加のセクションを示す次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="46ec2-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


