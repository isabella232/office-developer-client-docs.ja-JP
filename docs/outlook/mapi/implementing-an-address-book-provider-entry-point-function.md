---
title: アドレス帳プロバイダー エントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800924"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="88218-103">アドレス帳プロバイダー エントリ ポイント関数の実装</span><span class="sxs-lookup"><span data-stu-id="88218-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="88218-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88218-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88218-105">プロバイダーとその他のすべてのプロファイルの一部である場合、クライアント アプリケーションの呼び出し[MAPILogonEx](mapilogonex.md)アドレス帳プロバイダーが含まれているプロファイルを使用してセッションを開始するのには、MAPI を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="88218-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="88218-106">MAPI は、プロファイルを参照して、プロバイダーのエントリ ポイント関数の名前を学習します。</span><span class="sxs-lookup"><span data-stu-id="88218-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="88218-107">この関数ではありません、DLL エントリ ポイント関数と同じです。**DllMain**の Win32 のドキュメントでのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88218-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="88218-108">いくつかのエントリ、mapisvc.inf の構成ファイルにする必要があります、すべてのアドレス帳プロバイダーのプロファイルに含まれているがあります。</span><span class="sxs-lookup"><span data-stu-id="88218-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="88218-109">次の表は、これらのプロファイル] セクションのエントリと、mapisvc.inf ファイルが含める必要があるかどうかを一覧します。</span><span class="sxs-lookup"><span data-stu-id="88218-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="88218-110">**プロファイル セクションのエントリ**</span><span class="sxs-lookup"><span data-stu-id="88218-110">**Profile section entry**</span></span>|<span data-ttu-id="88218-111">**mapisvc.inf の要件**</span><span class="sxs-lookup"><span data-stu-id="88218-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88218-112">PR_DISPLAY_NAME =_文字列_</span><span class="sxs-lookup"><span data-stu-id="88218-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="88218-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="88218-113">Optional</span></span>  <br/> |
|<span data-ttu-id="88218-114">PR_PROVIDER_DISPLAY =_文字列_</span><span class="sxs-lookup"><span data-stu-id="88218-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="88218-115">必須</span><span class="sxs-lookup"><span data-stu-id="88218-115">Required</span></span>  <br/> |
|<span data-ttu-id="88218-116">PR_PROVIDER_DLL_NAME = _DLL のファイル名_</span><span class="sxs-lookup"><span data-stu-id="88218-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="88218-117">必須</span><span class="sxs-lookup"><span data-stu-id="88218-117">Required</span></span>  <br/> |
|<span data-ttu-id="88218-118">PR_RESOURCE_TYPE =_長_</span><span class="sxs-lookup"><span data-stu-id="88218-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="88218-119">必須</span><span class="sxs-lookup"><span data-stu-id="88218-119">Required</span></span>  <br/> |
|<span data-ttu-id="88218-120">PR_RESOURCE_FLAGS =_ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="88218-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="88218-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="88218-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="88218-122">プロファイル セクションの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すことによって直接または間接的に MAPISVC.INF を変更することによって、アドレス帳プロバイダーはプロファイルには、この情報を配置できます。</span><span class="sxs-lookup"><span data-stu-id="88218-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="88218-123">プロファイルは、MAPISVC に関連する情報を使用して構築されます。選択したサービス プロバイダーまたはサービスのメッセージの INF です。</span><span class="sxs-lookup"><span data-stu-id="88218-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="88218-124">詳細については、組織と MAPISVC の内容です。INF、 [MapiSvc.inf のファイル形式](file-format-of-mapisvc-inf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88218-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="88218-125">アドレス帳プロバイダーの DLL のエントリ ポイント関数の名前は[ABProviderInit](abproviderinit.md)である必要があり、 **ABProviderInit**のプロトタイプにそれに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="88218-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="88218-126">プロバイダーの DLL のエントリ ポイント関数では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="88218-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="88218-127">サービス プロバイダー インターフェイス (SPI) が MAPI を使用して、アドレス帳プロバイダーを使用しているバージョンと互換性のあるバージョンかどうかを確認するのにはのバージョンを確認してください。</span><span class="sxs-lookup"><span data-stu-id="88218-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="88218-128">アドレス帳プロバイダー オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="88218-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="88218-129">**生じます**か、 **MAPIUninitialize**をこの関数に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="88218-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="88218-130">DLL エントリ ポイント関数では、プロバイダー オブジェクトをインスタンス化し、MAPI にそのオブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="88218-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

