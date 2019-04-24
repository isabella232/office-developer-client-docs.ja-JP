---
title: アドレス帳プロバイダーエントリポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332803"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="7bc67-103">アドレス帳プロバイダーエントリポイント関数の実装</span><span class="sxs-lookup"><span data-stu-id="7bc67-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="7bc67-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bc67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bc67-105">クライアントアプリケーションが[MAPILogonEx](mapilogonex.md)を呼び出して、アドレス帳プロバイダーを含むプロファイルを使用してセッションを開始すると、MAPI はプロバイダーとプロファイルの一部である他のすべてを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="7bc67-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="7bc67-106">プロファイルを調べることによって、プロバイダーのエントリポイント関数の名前を MAPI が学習する。</span><span class="sxs-lookup"><span data-stu-id="7bc67-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="7bc67-107">この関数は DLL エントリポイント関数と同じではないことに注意してください。Win32 のドキュメントの\*\*\*\* ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bc67-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="7bc67-108">mapisvc.inf 構成ファイルにはいくつかのエントリがあり、すべてのアドレス帳プロバイダーのプロファイルセクションに含まれていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7bc67-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="7bc67-109">次の表に、これらのプロファイルセクションエントリと、mapisvc.inf ファイルにそれらを含める必要があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7bc67-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="7bc67-110">**プロファイルセクションエントリ**</span><span class="sxs-lookup"><span data-stu-id="7bc67-110">**Profile section entry**</span></span>|<span data-ttu-id="7bc67-111">**mapisvc.inf の要件**</span><span class="sxs-lookup"><span data-stu-id="7bc67-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bc67-112">PR_DISPLAY_NAME =_文字列_</span><span class="sxs-lookup"><span data-stu-id="7bc67-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="7bc67-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="7bc67-113">Optional</span></span>  <br/> |
|<span data-ttu-id="7bc67-114">PR_PROVIDER_DISPLAY =_文字列_</span><span class="sxs-lookup"><span data-stu-id="7bc67-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="7bc67-115">必須</span><span class="sxs-lookup"><span data-stu-id="7bc67-115">Required</span></span>  <br/> |
|<span data-ttu-id="7bc67-116">PR_PROVIDER_DLL_NAME = _DLL ファイル名_</span><span class="sxs-lookup"><span data-stu-id="7bc67-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="7bc67-117">必須</span><span class="sxs-lookup"><span data-stu-id="7bc67-117">Required</span></span>  <br/> |
|<span data-ttu-id="7bc67-118">PR_RESOURCE_TYPE = _long_</span><span class="sxs-lookup"><span data-stu-id="7bc67-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="7bc67-119">必須</span><span class="sxs-lookup"><span data-stu-id="7bc67-119">Required</span></span>  <br/> |
|<span data-ttu-id="7bc67-120">PR_RESOURCE_FLAGS =_ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="7bc67-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="7bc67-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="7bc67-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="7bc67-122">アドレス帳プロバイダーは、プロファイルセクションの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すか、mapisvc.inf を変更することによって、プロファイルにこの情報を直接配置できます。</span><span class="sxs-lookup"><span data-stu-id="7bc67-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="7bc67-123">プロファイルは、mapisvc.inf の関連情報を使用して作成されます。選択されたサービスプロバイダーまたはメッセージサービスの INF。</span><span class="sxs-lookup"><span data-stu-id="7bc67-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="7bc67-124">mapisvc.inf の組織と内容の詳細については、を参照してください。inf については、「 [File Format of mapisvc.inf](file-format-of-mapisvc-inf.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bc67-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="7bc67-125">アドレス帳プロバイダーの DLL エントリポイント関数の名前は、 [abproviderinit](abproviderinit.md)である必要があり、 **abproviderinit**プロトタイプに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bc67-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="7bc67-126">プロバイダーの DLL エントリポイント関数で次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bc67-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="7bc67-127">サービスプロバイダインターフェイス (SPI) のバージョンを調べて、MAPI が、アドレス帳プロバイダーが使用しているバージョンと互換性のあるバージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bc67-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="7bc67-128">アドレス帳プロバイダーオブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="7bc67-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="7bc67-129">この関数で**MAPIInitialize**または**MAPIUninitialize**のいずれかを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="7bc67-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="7bc67-130">DLL エントリポイント関数は、プロバイダーオブジェクトをインスタンス化し、そのオブジェクトへのポインターを MAPI に返します。</span><span class="sxs-lookup"><span data-stu-id="7bc67-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

