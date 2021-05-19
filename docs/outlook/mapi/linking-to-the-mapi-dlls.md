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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419304"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="2b295-103">MAPI DLL へのリンク</span><span class="sxs-lookup"><span data-stu-id="2b295-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="2b295-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b295-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b295-105">MAPI クライアントは **、LoadLibrary** 関数と **GetProcAddress** 関数を使用して、暗黙的に、または明示的Windows MAPI DLL にリンクできます。</span><span class="sxs-lookup"><span data-stu-id="2b295-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="2b295-106">MAPI DLL を明示的にリンクする方法については、「MAPI 関数への [リンク」を参照してください](how-to-link-to-mapi-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="2b295-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="2b295-107">MAPI は、MAPIX に型定義ステートメントを提供します。次の各関数の H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="2b295-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="2b295-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="2b295-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="2b295-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="2b295-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="2b295-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="2b295-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="2b295-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2b295-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2b295-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="2b295-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="2b295-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2b295-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2b295-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="2b295-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="2b295-115">MAPI DLL に明示的にリンクする場合は、これらの型定義を使用して、対応するエントリ ポイントを正しく呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2b295-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="2b295-116">サービス プロバイダーは、MAPI 以外の機能 (MAPI とは完全に関連しない機能) を DLL に含めできます。</span><span class="sxs-lookup"><span data-stu-id="2b295-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="2b295-117">これらの機能を使用する必要がある場合は **、DLL** と FreeLibrary を使用する前に **LoadLibrary** を呼び出して、使用後に DLL をメモリから削除します。</span><span class="sxs-lookup"><span data-stu-id="2b295-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="2b295-118">MAPI はサービス プロバイダー DLL の MAPI 以外の使用を知らないため、必要なときに DLL を使用できる保証はありません。</span><span class="sxs-lookup"><span data-stu-id="2b295-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="2b295-119">MAPI は、サービスを必要とするアクティブ なセッションを持つクライアントが存在しなくなった場合に、サービス プロバイダー DLL を解放します。</span><span class="sxs-lookup"><span data-stu-id="2b295-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

