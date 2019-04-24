---
title: mapisvc.inf でのサービスおよびサービスプロバイダーの登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: '最終更新日: 2013 年7月18日'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328372"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="b00da-103">mapisvc.inf でのサービスおよびサービスプロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="b00da-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="b00da-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b00da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b00da-105">システムに新しいプロバイダーをインストールするには、新しいプロバイダーをポイントするように mapisvc.inf ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b00da-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="b00da-106">構成中に設定される標準プロパティ。次のように、プロバイダーのダイナミックリンクライブラリ (.dll) を検索する場所を MAPI に通知します。</span><span class="sxs-lookup"><span data-stu-id="b00da-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="b00da-107">**PR_SERVICE_DLL_NAME**は **[Message SERVICE]** セクションで指定されます。</span><span class="sxs-lookup"><span data-stu-id="b00da-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="b00da-108">**PR_PROVIDER_DLL_NAME**は **[サービスプロバイダ]** セクションで指定されます。</span><span class="sxs-lookup"><span data-stu-id="b00da-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b00da-109">プロバイダーの .dll の名前 (サフィックスが "32" なし) を設定することが想定されています。</span><span class="sxs-lookup"><span data-stu-id="b00da-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="b00da-110">その後、MAPI は、そのパスでプロバイダーを検索することによってプロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="b00da-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="b00da-111">mapisvc.inf にパスを配置する</span><span class="sxs-lookup"><span data-stu-id="b00da-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="b00da-112">ほとんどのアプリケーションは、プログラムファイルの下にインストールされます。 MAPI プロバイダーが動作するようにするには、path 変数を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b00da-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="b00da-113">いくつかの制限により、Microsoft outlook 2010 と outlook 2013 は MAPI プロバイダーへの完全なパスに対応できます。</span><span class="sxs-lookup"><span data-stu-id="b00da-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="b00da-114">mapisvc.inf にプロバイダーを登録する場合、MAPI プロパティ**PR_SERVICE_DLL_NAME**および**PR_PROVIDER_DLL_NAME**にプロバイダーへの完全なパスを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b00da-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="b00da-115">どちらのプロパティでも、ファイルを検索する前にファイル名に追加されたままになるので、完全なパスはサフィックスが "32" でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b00da-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="b00da-116">これは、"c:\mypath\myprovider.dll" というパスを登録すると、MAPI が "c:\mypath\myprovider32.dll" を読み込もうとすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b00da-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="b00da-117">Outlook の MAPI は完全なパスに対応するように設計されていないため、文字列の最初のピリオドを検索することによって、"32" サフィックスを挿入します。これは、他のピリオドを含むパスを使用できないため、次のようなパスは使用できません。"c:\my.path\myprovider.dll" または "c:\mypath\my.provider.dll"。</span><span class="sxs-lookup"><span data-stu-id="b00da-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="b00da-118">ストアプロバイダーでは、 **WrapStoreEntryID**関数を使用してエントリ識別子を生成することもあります。これは、プロバイダーの名前をパラメーターとして取ります。</span><span class="sxs-lookup"><span data-stu-id="b00da-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b00da-119">mapisvc.inf で完全なパスを使用している場合は、 **WrapStoreEntryID**へのすべての呼び出しで同じパスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b00da-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="b00da-120">また、使用するパスは、 [getacp](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)関数によって提供されるコードページを使用して、Unicode との間で変換される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b00da-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="b00da-121">[MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/)および[WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)関数を使用して、このようなラウンドトリップを使用できない文字が含まれているパスを選択すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b00da-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="b00da-122">この機能のデモを行うために、GitHub でラップされた[PST サンプル](https://github.com/stephenegriffin/Outlook2010CodeSamples)が改訂されました。関連する機能は**MergeWithMapiSvc**および**generateproviderpath**にあります。</span><span class="sxs-lookup"><span data-stu-id="b00da-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

