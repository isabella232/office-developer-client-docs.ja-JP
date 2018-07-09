---
title: MapiSvc.inf のサービスおよびサービス ・ プロバイダーを登録します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: '最終更新日: 2013 年 7 月 18 日'
ms.openlocfilehash: 2eb7f1b496e0732b157ea4f9105a0e067329c52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803736"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="aa379-103">MapiSvc.inf のサービスおよびサービス ・ プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="aa379-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="aa379-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa379-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa379-105">システムに新しいプロバイダーをインストールするには、新しいプロバイダーを指すように、MapiSvc.inf ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa379-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="aa379-106">通知 MAPI プロバイダーのダイナミック リンク ライブラリ (.dll) を検索する場所の次のよう、標準のプロパティの構成中に設定します。</span><span class="sxs-lookup"><span data-stu-id="aa379-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="aa379-107">**PR_SERVICE_DLL_NAME**は、 **[メッセージ サービス]** セクションで指定されます。</span><span class="sxs-lookup"><span data-stu-id="aa379-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="aa379-108">**PR_PROVIDER_DLL_NAME**は、 **[サービス プロバイダー]** セクションで指定されます。</span><span class="sxs-lookup"><span data-stu-id="aa379-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="aa379-109">(32 のサフィックス) がない場合、プロバイダーの .dll の名前を設定することを予想にされます。</span><span class="sxs-lookup"><span data-stu-id="aa379-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="aa379-110">MAPI は、し、それを探すパス上で、プロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="aa379-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="aa379-111">MapiSvc.inf にパスを配置すること</span><span class="sxs-lookup"><span data-stu-id="aa379-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="aa379-112">[プログラム ファイル、MAPI プロバイダーが動作できるようにするのには path 変数の更新を必要とするほとんどのアプリケーションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="aa379-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="aa379-113">制限がいくつかの Microsoft Outlook 2010、Outlook 2013 は、MAPI プロバイダーに完全なパスに対応できます。</span><span class="sxs-lookup"><span data-stu-id="aa379-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="aa379-114">MapiSvc.inf のプロバイダーを登録すると、ときに**PR_SERVICE_DLL_NAME**と**PR_PROVIDER_DLL_NAME**は、MAPI プロパティのプロバイダーの完全なパスを配置する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aa379-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="aa379-115">いずれかのプロパティの完全なパス必要がありますサフィックス 32、MAPI は、ファイルを検索する前にファイル名を追加し続けるため。</span><span class="sxs-lookup"><span data-stu-id="aa379-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="aa379-116">つまり"c:\mypath\myprovider.dll"のパスを登録する場合は、MAPI がしようとする"c:\mypath\myprovider32.dll"を読み込めません。</span><span class="sxs-lookup"><span data-stu-id="aa379-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="aa379-117">Outlook の完全なパスに対応するために MAPI が想定されていません、つまり、他のピリオドを含むパスでは使用できません、次のようにパスを使用することはできませんので、文字列の最初の期間を検索しながらなどの挿入が行われます"c:\my.path\myprovider.dll"または"c:\mypath\my.provider.dll"です。</span><span class="sxs-lookup"><span data-stu-id="aa379-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="aa379-118">ストア プロバイダーのプロバイダーの名前をパラメーターとして受け取り、 **WrapStoreEntryID**関数を使用してエントリの識別子が生成されます。</span><span class="sxs-lookup"><span data-stu-id="aa379-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aa379-119">MapiSvc.inf の完全パスを使用する場合は、 **WrapStoreEntryID**への呼び出しで同じパスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa379-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="aa379-120">さらに、 [GetACP](http://msdn.microsoft.com/ja-jp/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)関数が用意されているコード ページを使用して Unicode との間に使用するパスを変換することがあります。</span><span class="sxs-lookup"><span data-stu-id="aa379-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](http://msdn.microsoft.com/ja-jp/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="aa379-121">[MultiByteToWideChar](http://msdn.microsoft.com/ja-jp/library/windows/desktop/dd319072%28v=vs.85%29.aspx/)と[WideCharToMultiByte](http://msdn.microsoft.com/ja-jp/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)関数を使用して、このようなラウンドト リップに対応できない文字を含むパスを選択する場合、障害が発生します。</span><span class="sxs-lookup"><span data-stu-id="aa379-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](http://msdn.microsoft.com/ja-jp/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](http://msdn.microsoft.com/ja-jp/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="aa379-122">この機能のデモでは、CodePlex で[ラップの PST のサンプル](http://ol2010mapisamples.codeplex.com/)が更新されました - **MergeWithMapiSvc**と**GenerateProviderPath**では、関連する機能です。</span><span class="sxs-lookup"><span data-stu-id="aa379-122">For a demonstration of this functionality, the [Wrapped PST sample](http://ol2010mapisamples.codeplex.com/) on CodePlex has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

