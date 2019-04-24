---
title: MAPI DLL へのリンク
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270043"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="c31d2-103">MAPI DLL へのリンク</span><span class="sxs-lookup"><span data-stu-id="c31d2-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="c31d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c31d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c31d2-105">mapi クライアントは、暗黙的に、または Windows 関数**LoadLibrary**と**GetProcAddress**を使用して明示的に mapi dll にリンクできます。</span><span class="sxs-lookup"><span data-stu-id="c31d2-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="c31d2-106">mapi dll を明示的にリンクする方法については、「 [mapi 関数へのリンク](how-to-link-to-mapi-functions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c31d2-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="c31d2-107">MAPI では、mapix に type definition ステートメントが用意されています。H ヘッダーファイルを次の各関数に対して使用します。</span><span class="sxs-lookup"><span data-stu-id="c31d2-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="c31d2-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="c31d2-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="c31d2-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="c31d2-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="c31d2-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="c31d2-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="c31d2-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c31d2-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c31d2-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c31d2-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="c31d2-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c31d2-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c31d2-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="c31d2-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="c31d2-115">これらの型定義を使用して、MAPI dll に明示的にリンクされている場合に、対応するエントリポイントを正しく呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c31d2-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="c31d2-116">サービスプロバイダーには、DLL で mapi 以外の機能 (mapi に完全に関連しない機能) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c31d2-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="c31d2-117">これらの機能を使用する必要がある場合は、dll と**FreeLibrary**を使用する前に**LoadLibrary**を呼び出して、使用した dll をメモリから削除します。</span><span class="sxs-lookup"><span data-stu-id="c31d2-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="c31d2-118">mapi は、サービスプロバイダー dll の非 mapi の使用を認識していないため、必要な場合に DLL が利用できるという保証はありません。</span><span class="sxs-lookup"><span data-stu-id="c31d2-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="c31d2-119">MAPI は、サービスを必要とするアクティブなセッションを持つクライアントがなくなったときに、サービスプロバイダー DLL を解放します。</span><span class="sxs-lookup"><span data-stu-id="c31d2-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

