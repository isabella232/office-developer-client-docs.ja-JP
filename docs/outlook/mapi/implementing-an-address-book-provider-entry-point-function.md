---
title: アドレス帳プロバイダーエントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409714"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="77315-103">アドレス帳プロバイダーエントリ ポイント関数の実装</span><span class="sxs-lookup"><span data-stu-id="77315-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="77315-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77315-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77315-105">クライアント アプリケーションが [MAPILogonEx](mapilogonex.md) を呼び出して、アドレス帳プロバイダーを含むプロファイルを使用してセッションを開始すると、MAPI はプロバイダーとプロファイルの一部である他のすべてのユーザーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="77315-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="77315-106">MAPI は、プロファイルを見て、プロバイダーのエントリ ポイント関数の名前を学習します。</span><span class="sxs-lookup"><span data-stu-id="77315-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="77315-107">この関数は DLL エントリ ポイント関数と同じではありません。Win32 のドキュメント **の DllMain** のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77315-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="77315-108">mapisvc.inf 構成ファイルに表示する必要があるエントリは、いくつかのエントリで、すべてのアドレス帳プロバイダーのプロファイル セクションに含まれています。</span><span class="sxs-lookup"><span data-stu-id="77315-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="77315-109">次の表に、これらのプロファイル セクション エントリと、mapisvc.inf ファイルに含める必要があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="77315-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="77315-110">**プロファイル セクションのエントリ**</span><span class="sxs-lookup"><span data-stu-id="77315-110">**Profile section entry**</span></span>|<span data-ttu-id="77315-111">**mapisvc.inf の要件**</span><span class="sxs-lookup"><span data-stu-id="77315-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77315-112">PR_DISPLAY_NAME= _string_</span><span class="sxs-lookup"><span data-stu-id="77315-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="77315-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="77315-113">Optional</span></span>  <br/> |
|<span data-ttu-id="77315-114">PR_PROVIDER_DISPLAY= _string_</span><span class="sxs-lookup"><span data-stu-id="77315-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="77315-115">必須</span><span class="sxs-lookup"><span data-stu-id="77315-115">Required</span></span>  <br/> |
|<span data-ttu-id="77315-116">PR_PROVIDER_DLL_NAME= _DLL ファイル名_</span><span class="sxs-lookup"><span data-stu-id="77315-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="77315-117">必須</span><span class="sxs-lookup"><span data-stu-id="77315-117">Required</span></span>  <br/> |
|<span data-ttu-id="77315-118">PR_RESOURCE_TYPE= _long_</span><span class="sxs-lookup"><span data-stu-id="77315-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="77315-119">必須</span><span class="sxs-lookup"><span data-stu-id="77315-119">Required</span></span>  <br/> |
|<span data-ttu-id="77315-120">PR_RESOURCE_FLAGS= _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="77315-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="77315-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="77315-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="77315-122">アドレス帳プロバイダーは、プロファイル セクションの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出すことによって、または MAPISVC.INF を変更することで間接的に、この情報をプロファイルに直接配置できます。</span><span class="sxs-lookup"><span data-stu-id="77315-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="77315-123">プロファイルは、MAPISVC の関連情報を使用して構築されます。選択したサービス プロバイダーまたはメッセージ サービスの INF。</span><span class="sxs-lookup"><span data-stu-id="77315-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="77315-124">MAPISVC の組織とコンテンツの詳細については、次の情報を参照してください。 [INF、MapiSvc.inf のファイル形式を参照してください](file-format-of-mapisvc-inf.md)。</span><span class="sxs-lookup"><span data-stu-id="77315-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="77315-125">アドレス帳プロバイダーの DLL エントリ ポイント関数の名前は [ABProviderInit](abproviderinit.md) で **、ABProviderInit** プロトタイプに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="77315-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="77315-126">プロバイダーの DLL エントリ ポイント関数で次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="77315-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="77315-127">サービス プロバイダー インターフェイス (SPI) のバージョンを確認して、MAPI がアドレス帳プロバイダーが使用しているバージョンと互換性のあるバージョンを使用している必要があります。</span><span class="sxs-lookup"><span data-stu-id="77315-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="77315-128">アドレス帳プロバイダー オブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="77315-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="77315-129">この関数では **、MAPIInitialize または** **MAPIUninitialize を呼** び出さません。</span><span class="sxs-lookup"><span data-stu-id="77315-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="77315-130">DLL エントリ ポイント関数は、プロバイダー オブジェクトをインスタンス化し、そのオブジェクトへのポインターを MAPI に返します。</span><span class="sxs-lookup"><span data-stu-id="77315-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

