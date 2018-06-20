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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="ede64-103">MapiSvc.inf のメッセージ サービスのセクションで、リストのエントリ</span><span class="sxs-lookup"><span data-stu-id="ede64-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="ede64-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ede64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ede64-105">セクションのリストのエントリの 2 種類があります: サービス プロバイダー セクションおよびその他のメッセージ サービスに固有のセクションを一覧表示する一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="ede64-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="ede64-106">Mapisvc.inf の以下のファイル形式でこれらの 2 種類のエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ede64-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="ede64-107">**プロバイダー**エントリ内の各セクションは、メッセージ サービスが属するサービス ・ プロバイダーの構成情報を提供する個々 のセクションにマップされます。</span><span class="sxs-lookup"><span data-stu-id="ede64-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="ede64-108">**セクション**エントリ内の各セクションは、メッセージ サービスで必要となる余分な構成情報を含むセクションにマップされます。</span><span class="sxs-lookup"><span data-stu-id="ede64-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="ede64-109">メッセージ サービスの実装者は、標準のセクションに適合しない特殊な情報が含まれている場合、余分なセクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="ede64-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="ede64-110">複雑な構成通常メッセージ サービスでは、余分な情報を追加するのに**セクション**のエントリを使用します。</span><span class="sxs-lookup"><span data-stu-id="ede64-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="ede64-111">メッセージ サービスのすべてのセクションには、**プロバイダー**のエントリのリストに少なくとも 1 つのセクションでメッセージ サービスのすべてのセクションでは、**セクション**のエントリがあります。</span><span class="sxs-lookup"><span data-stu-id="ede64-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="ede64-112">メッセージ サービスのセクションの 2 つの例に従います。</span><span class="sxs-lookup"><span data-stu-id="ede64-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="ede64-113">最初のセクションでは、図では、1 つのサービス プロバイダーの簡単なメッセージ サービスからアドレス帳の既定のサービスのこと。</span><span class="sxs-lookup"><span data-stu-id="ede64-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="ede64-114">2 番目のセクションは、MsgService サービスは、次の 3 つのサービス プロバイダーとのより複雑なサンプル メッセージ サービスです。</span><span class="sxs-lookup"><span data-stu-id="ede64-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="ede64-115">**[MsgService]** セクションの**セクション**のエントリの一覧の他の 2 つのセクション、1 つと呼ばれる **[First_Special_Section]** と **[Second_Special_Section]** と呼ばれる別のです。</span><span class="sxs-lookup"><span data-stu-id="ede64-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="ede64-116">余分なセクション内に表示されるデータは、特定のメッセージ サービスに有効です。</span><span class="sxs-lookup"><span data-stu-id="ede64-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="ede64-117">これらのセクションには、余分なセクションを説明するために次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ede64-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


