---
title: MapiSvc.inf でのサービスとサービス プロバイダーの登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: '最終更新日: 2013 年 7 月 18 日'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328372"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="08ca7-103">MapiSvc.inf でのサービスとサービス プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="08ca7-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="08ca7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08ca7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08ca7-105">システムに新しいプロバイダーをインストールするには、MapiSvc.inf ファイルを更新して新しいプロバイダーをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ca7-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="08ca7-106">構成時に設定される標準プロパティ (以下を含む) は、プロバイダーの動的リンク ライブラリを見つける場所を MAPI に通知します (.dll)。</span><span class="sxs-lookup"><span data-stu-id="08ca7-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="08ca7-107">この **PR_SERVICE_DLL_NAME** [Message **Service] セクションで指定** します。</span><span class="sxs-lookup"><span data-stu-id="08ca7-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="08ca7-108">この **PR_PROVIDER_DLL_NAME** [サービス プロバイダー] **セクションで指定** します。</span><span class="sxs-lookup"><span data-stu-id="08ca7-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="08ca7-109">期待される点は、プロバイダーの名前を (サフィックス "32" .dll付けずに) 設定するということです。</span><span class="sxs-lookup"><span data-stu-id="08ca7-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="08ca7-110">MAPI は、パスでプロバイダーを探して、プロバイダーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="08ca7-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="08ca7-111">MapiSvc.inf にパスを入れる</span><span class="sxs-lookup"><span data-stu-id="08ca7-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="08ca7-112">ほとんどのアプリケーションは Program Files の下にインストールされ、MAPI プロバイダーが動作するためにパス変数を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ca7-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="08ca7-113">いくつかの制限により、Microsoft Outlook 2010 Outlook 2013 は MAPI プロバイダーへの完全なパスに対応できます。</span><span class="sxs-lookup"><span data-stu-id="08ca7-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="08ca7-114">MapiSvc.inf にプロバイダーを登録する場合は、MAPI プロパティおよび MAPI プロパティにプロバイダーへの完全なパスPR_SERVICE_DLL_NAME **置** PR_PROVIDER_DLL_NAME。</span><span class="sxs-lookup"><span data-stu-id="08ca7-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="08ca7-115">どちらのプロパティでも、MAPI はファイルを探す前にファイル名に追加し続けるので、完全パスには接尾辞 "32" を付けない必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ca7-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="08ca7-116">つまり、"c:\mypath\myprovider.dll" パスを登録すると、MAPI は "c:\mypath\myprovider32.dll" を読み込c:\mypath\myprovider32.dll。</span><span class="sxs-lookup"><span data-stu-id="08ca7-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="08ca7-117">Outlook の MAPI はもともと完全なパスに対応するように設計されていたため、文字列の最初のピリオドを探して"32" サフィックスを挿入します。つまり、他の期間を含むパスは機能しないので、"c:\my.path\myprovider.dll" や "c:\mypath\my.provider.dll" などのパスを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="08ca7-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="08ca7-118">ストア プロバイダーでは **、WrapStoreEntryID** 関数を使用してエントリ識別子を生成し、プロバイダーの名前をパラメーターとして受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="08ca7-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="08ca7-119">MapiSvc.inf でフル パスを使用している場合は **、WrapStoreEntryID** の呼び出しで同じパスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ca7-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="08ca7-120">さらに [、GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) 関数によって提供されるコード ページを使用して、使用するパスを Unicode に変換して Unicode から変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="08ca7-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="08ca7-121">[MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/)関数と[WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)関数を通じてこのようなラウンドトリップを生き残れない文字を含むパスを選択すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="08ca7-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="08ca7-122">この機能のデモンストレーションでは、GitHub のラップ [された PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) サンプルが改訂されました。関連する機能は **MergeWithMapiSvc** および **GenerateProviderPath** にあります。</span><span class="sxs-lookup"><span data-stu-id="08ca7-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

