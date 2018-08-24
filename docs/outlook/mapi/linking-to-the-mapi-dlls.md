---
title: MAPI DLL へのリンク
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582029"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="e8fd0-103">MAPI DLL へのリンク</span><span class="sxs-lookup"><span data-stu-id="e8fd0-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="e8fd0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8fd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8fd0-105">MAPI クライアントにリンクできます MAPI Dll、暗黙的にまたは明示的に Windows 関数**LoadLibrary**と**GetProcAddress**を使用しています。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="e8fd0-106">MAPI Dll を明示的にリンクする方法の詳細については、 [MAPI の関数へのリンク](how-to-link-to-mapi-functions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="e8fd0-107">MAPI には、MAPIX の種類の定義ステートメントが用意されています。H のヘッダー ファイルの次の関数の:</span><span class="sxs-lookup"><span data-stu-id="e8fd0-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="e8fd0-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="e8fd0-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="e8fd0-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="e8fd0-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="e8fd0-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="e8fd0-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="e8fd0-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e8fd0-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e8fd0-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="e8fd0-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="e8fd0-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e8fd0-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e8fd0-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="e8fd0-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="e8fd0-115">MAPI Dll に明示的にリンクする場合に正しく対応するエントリ ポイントを呼び出すには、これらの型定義を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="e8fd0-116">サービス プロバイダーは、非 MAPI 機能を含めることができます-は、MAPI とはまったく関係のない機能-その DLL にします。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="e8fd0-117">これらの機能を使用する場合は、 **LoadLibrary**を使用した後、DLL をメモリから削除するのには**終わった**DLL を使用する前に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="e8fd0-118">MAPI がサービス ・ プロバイダー DLL の MAPI 以外の使用方法を認識しないので、DLL が必要なときに利用できるという保証はありません。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="e8fd0-119">MAPI は、不要になったすべてのクライアントにサービスを必要とするアクティブなセッションがある場合に、サービス プロバイダーの DLL を解放します。</span><span class="sxs-lookup"><span data-stu-id="e8fd0-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

