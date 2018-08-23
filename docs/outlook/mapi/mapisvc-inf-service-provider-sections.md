---
title: MapiSvc.inf サービス プロバイダーセクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586782"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="21695-103">MapiSvc.inf サービス プロバイダーセクション</span><span class="sxs-lookup"><span data-stu-id="21695-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="21695-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21695-105">Mapisvc.inf には、メッセージ サービスの前のセクションで**プロバイダー**のエントリに記載されているエントリのそれぞれのサービス プロバイダーの 1 つのセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="21695-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="21695-106">**サービス**プロバイダー セクションと似ていますがメッセージ サービスのセクションでセクションの両方の種類には、この形式のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="21695-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="21695-107">**プロパティ タグ**プロパティの値を =</span><span class="sxs-lookup"><span data-stu-id="21695-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="21695-108">ただし、サービスのプロバイダー セクションで、メッセージ サービスのセクションとは異なりそのようなプロパティのエントリは、サービスのプロバイダー セクションに含まれているエントリの種類。</span><span class="sxs-lookup"><span data-stu-id="21695-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="21695-109">必要があります追加またはリンクのセクションで、サービス プロバイダーです。1 つのセクション内では、すべてのサービス プロバイダーの情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="21695-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="21695-110">メッセージ サービスのセクションで設定されているプロパティのいくつかは、これらのプロパティは、両方の意味を行うために、サービス プロバイダーのセクションで設定もできます。</span><span class="sxs-lookup"><span data-stu-id="21695-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="21695-111">**PR_DISPLAY_NAME**プロパティは、例です。</span><span class="sxs-lookup"><span data-stu-id="21695-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="21695-112">構成のユーザー インターフェイスに表示するために使用される名前は、サービス プロバイダーとサービスのメッセージの両方であります。</span><span class="sxs-lookup"><span data-stu-id="21695-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="21695-113">サービス プロバイダーによってその名可能性がありますか、同じことができません。</span><span class="sxs-lookup"><span data-stu-id="21695-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="21695-114">その他のプロパティは、サービス ・ プロバイダーに固有です。</span><span class="sxs-lookup"><span data-stu-id="21695-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="21695-115">プロバイダー セクションの一般的なサービスには、必要なすべてが、次のエントリがあります。</span><span class="sxs-lookup"><span data-stu-id="21695-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="21695-116">**PR_DISPLAY_NAME** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="21695-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="21695-117">**PR_PROVIDER_DISPLAY** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="21695-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="21695-118">**PR_PROVIDER_DLL_NAME** =  _DLL ファイルの名前_</span><span class="sxs-lookup"><span data-stu-id="21695-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="21695-119">**PR_RESOURCE_TYPE** =  _長_</span><span class="sxs-lookup"><span data-stu-id="21695-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="21695-120">**PR_RESOURCE_FLAGS** =  _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="21695-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="21695-121">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) のエントリが**PR_SERVICE_DLL_NAME**に似ています。サービス プロバイダーを含む DLL のファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="21695-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="21695-122">メッセージ サービスのコードは、同じ DLL ファイル内のサービス ・ プロバイダーのいずれかで保存することがありますか、別の DLL として存在しています。</span><span class="sxs-lookup"><span data-stu-id="21695-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="21695-123">ターゲット プラットフォームに関係なく、エントリにサフィックスが含まれていないことに注意してください。MAPI の必要な場合にサフィックスを追加することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="21695-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="21695-124">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md)) のエントリは、サービス プロバイダーの種類を表します。サービス プロバイダーは、適切な定義済みの定数を設定します。</span><span class="sxs-lookup"><span data-stu-id="21695-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="21695-125">有効な値には、MAPI_STORE_PROVIDER、MAPI_TRANSPORT_PROVIDER、および MAPI_AB_PROVIDER が含まれます。</span><span class="sxs-lookup"><span data-stu-id="21695-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="21695-126">メッセージ サービスおよびサービス ・ プロバイダーの両方に適用される他のプロパティ エントリ、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のエントリは、オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="21695-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="21695-127">このプロパティのエントリの設定は、サービス プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="21695-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="21695-128">たとえば、メッセージ ストアのプロバイダーによって設定**PR_RESOURCE_FLAGS** STATUS_NO_DEFAULT_STORE に既定のメッセージ ストアとして動作しない場合。</span><span class="sxs-lookup"><span data-stu-id="21695-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="21695-129">サービス プロバイダー セクションの 3 つの例に従います。</span><span class="sxs-lookup"><span data-stu-id="21695-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="21695-130">**[AB プロバイダー]** セクションでは、既定のアドレス帳サービスのサービス プロバイダーのセクションです。</span><span class="sxs-lookup"><span data-stu-id="21695-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="21695-131">**[MsgService Prov1]** と **[MsgService Prov2]** セクションでは、自分独自のサービスです。最初のアドレス帳のプロバイダー セクションでは、2 番目のメッセージ ストア プロバイダー セクションです。</span><span class="sxs-lookup"><span data-stu-id="21695-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


