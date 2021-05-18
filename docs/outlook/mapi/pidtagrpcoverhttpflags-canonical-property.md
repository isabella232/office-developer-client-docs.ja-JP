---
title: PidTagRpcOverHttpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327448"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="d2196-103">PidTagRpcOverHttpFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2196-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d2196-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2196-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2196-105">ハイパーテキスト転送プロトコル (HTTP) をMicrosoft Office Outlookリモート プロシージャ 呼び出し (RPC) を使用Microsoft Exchange Serverに接続するために使用されるプロファイルの設定が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d2196-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2196-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d2196-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2196-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d2196-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d2196-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d2196-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2196-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="d2196-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="d2196-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d2196-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2196-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d2196-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d2196-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d2196-112">Area:</span></span>  <br/> |<span data-ttu-id="d2196-113">その他</span><span class="sxs-lookup"><span data-stu-id="d2196-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2196-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d2196-114">Remarks</span></span>

<span data-ttu-id="d2196-115">PR_ROH_FLAGS **プロパティ** は、メッセージング アプリケーション プログラミング インターフェイス (MAPI) プロファイルのグローバル プロファイル セクションに格納されます。</span><span class="sxs-lookup"><span data-stu-id="d2196-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="d2196-116">PR_ROH_FLAGSの **値** は、次のフラグの 1 つ以上で構成されるビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d2196-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="d2196-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="d2196-117">**Name**</span></span>|<span data-ttu-id="d2196-118">**値**</span><span class="sxs-lookup"><span data-stu-id="d2196-118">**Value**</span></span>|<span data-ttu-id="d2196-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d2196-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2196-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="d2196-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="d2196-121">0x1</span><span class="sxs-lookup"><span data-stu-id="d2196-121">0x1</span></span>  <br/> |<span data-ttu-id="d2196-122">Connect HTTP を使用してExchange Serverにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d2196-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="d2196-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="d2196-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="d2196-124">0x2</span><span class="sxs-lookup"><span data-stu-id="d2196-124">0x2</span></span>  <br/> |<span data-ttu-id="d2196-125">Connectソケット層 (SSL) Exchange Serverを使用してサーバーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d2196-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="d2196-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="d2196-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="d2196-127">0x4</span><span class="sxs-lookup"><span data-stu-id="d2196-127">0x4</span></span>  <br/> |<span data-ttu-id="d2196-128">SSL を使用して接続するときに、セッションを相互に認証します。</span><span class="sxs-lookup"><span data-stu-id="d2196-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="d2196-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="d2196-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="d2196-130">0x8</span><span class="sxs-lookup"><span data-stu-id="d2196-130">0x8</span></span>  <br/> |<span data-ttu-id="d2196-131">高速ネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="d2196-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="d2196-132">次に、TCP/IP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="d2196-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="d2196-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="d2196-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="d2196-134">0x20</span><span class="sxs-lookup"><span data-stu-id="d2196-134">0x20</span></span>  <br/> |<span data-ttu-id="d2196-135">低速ネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="d2196-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="d2196-136">次に、TCP/IP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="d2196-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="d2196-137">たとえば、HTTP で RPC を有効にし、SSL を要求し、低速接続で最初に HTTP プロトコルを使用する必要がある場合は **、PR_ROH_FLAGS PR_ROH_FLAGS** プロパティの値を **0x23** に設定します。 `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`</span><span class="sxs-lookup"><span data-stu-id="d2196-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d2196-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d2196-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2196-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d2196-139">Protocol specifications</span></span>

<span data-ttu-id="d2196-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2196-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2196-141">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="d2196-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2196-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2196-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2196-143">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="d2196-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="d2196-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2196-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2196-145">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2196-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2196-146">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d2196-146">Header files</span></span>

<span data-ttu-id="d2196-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2196-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2196-148">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2196-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2196-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2196-149">Mapitags.h</span></span>
  
> <span data-ttu-id="d2196-150">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d2196-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2196-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2196-151">See also</span></span>



[<span data-ttu-id="d2196-152">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d2196-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2196-153">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2196-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2196-154">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d2196-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2196-155">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d2196-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

