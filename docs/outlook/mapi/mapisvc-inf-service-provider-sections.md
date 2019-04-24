---
title: mapisvc.inf サービスプロバイダーのセクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309542"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="f29e9-103">mapisvc.inf サービスプロバイダーのセクション</span><span class="sxs-lookup"><span data-stu-id="f29e9-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="f29e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f29e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f29e9-105">mapisvc.inf には、前の「メッセージサービス」セクションの**プロバイダ**エントリにリストされている各エントリのサービスプロバイダセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f29e9-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="f29e9-106">**サービス**プロバイダーのセクションは、両方の種類のセクションに次の形式のエントリが含まれているという点で、メッセージサービスセクションに似ています。</span><span class="sxs-lookup"><span data-stu-id="f29e9-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="f29e9-107">**プロパティタグ**= プロパティ値</span><span class="sxs-lookup"><span data-stu-id="f29e9-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="f29e9-108">ただし、サービスプロバイダーのセクションとメッセージサービスのセクションは、このようなプロパティエントリがサービスプロバイダーセクションに含まれるエントリの唯一の種類であるという点で異なります。</span><span class="sxs-lookup"><span data-stu-id="f29e9-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="f29e9-109">サービスプロバイダーには、追加またはリンクされたセクションはありません。すべてのサービスプロバイダー情報は、1つのセクション内に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f29e9-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="f29e9-110">[メッセージサービス] セクションで設定されているプロパティの一部は、[サービスプロバイダ] セクションでも設定されています。これらのプロパティは両方にとって有効です。</span><span class="sxs-lookup"><span data-stu-id="f29e9-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="f29e9-111">**PR_DISPLAY_NAME**プロパティの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f29e9-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="f29e9-112">サービスプロバイダーとメッセージサービスの両方には、構成ユーザーインターフェイスでの表示に使用される名前があります。</span><span class="sxs-lookup"><span data-stu-id="f29e9-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="f29e9-113">この名前は、サービスプロバイダーによって異なりますが、同じでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="f29e9-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="f29e9-114">その他のプロパティは、サービスプロバイダーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="f29e9-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="f29e9-115">サービスプロバイダーの一般的なセクションには、次のエントリが含まれています。これらはすべて必要です。</span><span class="sxs-lookup"><span data-stu-id="f29e9-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="f29e9-116">**PR_DISPLAY_NAME** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="f29e9-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="f29e9-117">**PR_PROVIDER_DISPLAY** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="f29e9-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="f29e9-118">\*\*\*\* =  _DLL ファイルの PR_PROVIDER_DLL_NAME 名_</span><span class="sxs-lookup"><span data-stu-id="f29e9-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="f29e9-119">**PR_RESOURCE_TYPE** =  _long_</span><span class="sxs-lookup"><span data-stu-id="f29e9-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="f29e9-120">**PR_RESOURCE_FLAGS** =  _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="f29e9-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="f29e9-121">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) エントリは**PR_SERVICE_DLL_NAME**に似ています。これは、サービスプロバイダーを含む DLL のファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="f29e9-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="f29e9-122">メッセージサービスコードは、サービスプロバイダーの1つと同じ dll ファイルに格納するか、別の dll として存在することができます。</span><span class="sxs-lookup"><span data-stu-id="f29e9-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="f29e9-123">ターゲットプラットフォームに関係なく、エントリにサフィックスが含まれていないことに注意してください。MAPI は必要に応じてサフィックスを追加します。</span><span class="sxs-lookup"><span data-stu-id="f29e9-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="f29e9-124">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry は、サービスプロバイダーの種類を表します。サービスプロバイダーは、それを適切な定義済みの定数に設定します。</span><span class="sxs-lookup"><span data-stu-id="f29e9-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="f29e9-125">有効な値は、MAPI_STORE_PROVIDER、MAPI_TRANSPORT_PROVIDER、および MAPI_AB_PROVIDER です。</span><span class="sxs-lookup"><span data-stu-id="f29e9-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="f29e9-126">メッセージサービスとサービスプロバイダーの両方に適用される別のプロパティエントリは、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリがオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="f29e9-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="f29e9-127">このプロパティエントリの設定は、サービスプロバイダーによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f29e9-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="f29e9-128">たとえば、一部のメッセージストアプロバイダーでは、 **PR_RESOURCE_FLAGS**が既定のメッセージストアとして機能しない場合、STATUS_NO_DEFAULT_STORE に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="f29e9-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="f29e9-129">次に、サービスプロバイダーセクションの3つの例を示します。</span><span class="sxs-lookup"><span data-stu-id="f29e9-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="f29e9-130">**[AB provider]** セクションは、既定のアドレス帳サービスのサービスプロバイダーセクションです。</span><span class="sxs-lookup"><span data-stu-id="f29e9-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="f29e9-131">**[msgservice Prov1]** および **[msgservice Prov2]** セクションは、自分のサービスに属しています。1つ目はアドレス帳プロバイダーセクションで、2つ目はメッセージストアプロバイダーセクションです。</span><span class="sxs-lookup"><span data-stu-id="f29e9-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
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


