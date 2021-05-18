---
title: MapiSvc.inf サービス プロバイダーのセクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405563"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="3e214-103">MapiSvc.inf サービス プロバイダーのセクション</span><span class="sxs-lookup"><span data-stu-id="3e214-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="3e214-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e214-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e214-105">Mapisvc.inf には、前のメッセージ サービス セクションの **Providers** エントリに記載されている各エントリに対して 1 つのサービス プロバイダー セクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e214-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="3e214-106">**サービス** プロバイダー のセクションは、両方の種類のセクションにこの形式のエントリが含まれるという点で、メッセージ サービス セクションに似ています。</span><span class="sxs-lookup"><span data-stu-id="3e214-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="3e214-107">**プロパティ タグ** = プロパティ値</span><span class="sxs-lookup"><span data-stu-id="3e214-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="3e214-108">ただし、サービス プロバイダー セクションとメッセージ サービス セクションは、このようなプロパティ エントリがサービス プロバイダー セクションに含まれる唯一の種類のエントリである点で異なります。</span><span class="sxs-lookup"><span data-stu-id="3e214-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="3e214-109">サービス プロバイダーの追加またはリンクされたセクションはありません。すべてのサービス プロバイダー情報は、1 つのセクションに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e214-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="3e214-110">これらのプロパティは両方とも意味を持つため、メッセージ サービス セクションで設定されているプロパティの一部は、サービス プロバイダー セクションでも設定されます。</span><span class="sxs-lookup"><span data-stu-id="3e214-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="3e214-111">プロパティ **PR_DISPLAY_NAME** 例を示します。</span><span class="sxs-lookup"><span data-stu-id="3e214-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="3e214-112">サービス プロバイダーとメッセージ サービスの両方に、構成ユーザー インターフェイスでの表示に使用される名前があります。</span><span class="sxs-lookup"><span data-stu-id="3e214-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="3e214-113">サービス プロバイダーによっては、その名前が同じか異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e214-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="3e214-114">その他のプロパティは、サービス プロバイダーに固有です。</span><span class="sxs-lookup"><span data-stu-id="3e214-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="3e214-115">一般的なサービス プロバイダー のセクションには、次のエントリが含まれます。そのすべてが必須です。</span><span class="sxs-lookup"><span data-stu-id="3e214-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="3e214-116">**PR_DISPLAY_NAME**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="3e214-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="3e214-117">**PR_PROVIDER_DISPLAY**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="3e214-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="3e214-118">**PR_PROVIDER_DLL_NAME**  =  _DLL ファイルの名前_</span><span class="sxs-lookup"><span data-stu-id="3e214-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="3e214-119">**PR_RESOURCE_TYPE**  =  _long_</span><span class="sxs-lookup"><span data-stu-id="3e214-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="3e214-120">**PR_RESOURCE_FLAGS**  =  _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="3e214-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="3e214-121">この **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) エントリは、次の **PR_SERVICE_DLL_NAME。** サービス プロバイダーを含む DLL のファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="3e214-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="3e214-122">メッセージ サービス コードは、サービス プロバイダーの 1 つを同じ DLL ファイルに格納するか、別の DLL として存在することができます。</span><span class="sxs-lookup"><span data-stu-id="3e214-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="3e214-123">ターゲット プラットフォームに関係なく、エントリに接尾辞が含まれていない点に注意してください。MAPI は、必要に応じて接尾辞の追加を行います。</span><span class="sxs-lookup"><span data-stu-id="3e214-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="3e214-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) エントリは、サービス プロバイダーの種類を表します。サービス プロバイダーは、それを適切な定義済みの定数に設定します。</span><span class="sxs-lookup"><span data-stu-id="3e214-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="3e214-125">有効な値には、MAPI_STORE_PROVIDER、MAPI_TRANSPORT_PROVIDER、およびMAPI_AB_PROVIDER。</span><span class="sxs-lookup"><span data-stu-id="3e214-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="3e214-126">メッセージ サービスとサービス プロバイダーの両方に適用される別のプロパティ エントリで、PR_RESOURCE_FLAGS **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリはオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="3e214-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="3e214-127">このプロパティ エントリの設定は、サービス プロバイダーによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e214-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="3e214-128">たとえば、一部のメッセージ ストア プロバイダーは、既定のメッセージ PR_RESOURCE_FLAGSとしてSTATUS_NO_DEFAULT_STORE機能しない場合に、メッセージ ストアプロバイダーを既定のメッセージ ストアに設定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e214-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="3e214-129">サービス プロバイダーセクションの 3 つの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3e214-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="3e214-130">[AB **プロバイダー] セクションは** 、既定のアドレス帳サービスのサービス プロバイダー セクションです。</span><span class="sxs-lookup"><span data-stu-id="3e214-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="3e214-131">**[MsgService Prov1] セクションと** **[MsgService Prov2]** セクションは、My Own Service に属します。1 つ目はアドレス帳プロバイダー セクションで、2 つ目はメッセージ ストア プロバイダー セクションです。</span><span class="sxs-lookup"><span data-stu-id="3e214-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
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


