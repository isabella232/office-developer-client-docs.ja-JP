---
title: PidTagRpcOverHttpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b36f71958528b25829b1ff85b29572b3590f9d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594818"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="35b6d-103">PidTagRpcOverHttpFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35b6d-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="35b6d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35b6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35b6d-105">ハイパー テキスト転送プロトコル (HTTP) 経由でリモート プロシージャ コール (RPC) を使用して Microsoft Exchange Server に接続する Microsoft Office Outlook で使用されるプロファイルの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35b6d-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35b6d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="35b6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35b6d-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="35b6d-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="35b6d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="35b6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35b6d-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="35b6d-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="35b6d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="35b6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="35b6d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="35b6d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="35b6d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="35b6d-112">Area:</span></span>  <br/> |<span data-ttu-id="35b6d-113">その他</span><span class="sxs-lookup"><span data-stu-id="35b6d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35b6d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="35b6d-114">Remarks</span></span>

<span data-ttu-id="35b6d-115">**PR_ROH_FLAGS**プロパティは、メッセージング アプリケーション プログラミング インターフェイス (MAPI) プロファイルのグローバル プロファイル セクションに格納されます。</span><span class="sxs-lookup"><span data-stu-id="35b6d-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="35b6d-116">**PR_ROH_FLAGS**の値は、次のフラグの 1 つ以上で構成されるビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="35b6d-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="35b6d-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="35b6d-117">**Name**</span></span>|<span data-ttu-id="35b6d-118">**値**</span><span class="sxs-lookup"><span data-stu-id="35b6d-118">**Value**</span></span>|<span data-ttu-id="35b6d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="35b6d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35b6d-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="35b6d-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="35b6d-121">0x1</span><span class="sxs-lookup"><span data-stu-id="35b6d-121">0x1</span></span>  <br/> |<span data-ttu-id="35b6d-122">HTTP 経由で RPC を使用して Exchange Server に接続します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="35b6d-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="35b6d-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="35b6d-124">0x2</span><span class="sxs-lookup"><span data-stu-id="35b6d-124">0x2</span></span>  <br/> |<span data-ttu-id="35b6d-125">セキュア ソケット レイヤー (SSL) のみを使用して Exchange Server に接続します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="35b6d-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="35b6d-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="35b6d-127">0x4</span><span class="sxs-lookup"><span data-stu-id="35b6d-127">0x4</span></span>  <br/> |<span data-ttu-id="35b6d-128">セッションを相互認証で SSL を使用して接続するとき。</span><span class="sxs-lookup"><span data-stu-id="35b6d-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="35b6d-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="35b6d-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="35b6d-130">0x8</span><span class="sxs-lookup"><span data-stu-id="35b6d-130">0x8</span></span>  <br/> |<span data-ttu-id="35b6d-131">高速ネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="35b6d-132">TCP/IP を使用して接続し、します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="35b6d-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="35b6d-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="35b6d-134">0x20</span><span class="sxs-lookup"><span data-stu-id="35b6d-134">0x20</span></span>  <br/> |<span data-ttu-id="35b6d-135">低速ネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="35b6d-136">TCP/IP を使用して接続し、します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="35b6d-137">たとえば、 **PR_ROH_FLAGS**を設定するのにを RPC over HTTP、SSL を要求して、低速接続で HTTP プロトコルを最初に使用することを指定する有効にするプロパティの値を設定、 **PR_ROH_FLAGS**プロパティを`ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`0x23 に等しいであります。</span><span class="sxs-lookup"><span data-stu-id="35b6d-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35b6d-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="35b6d-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35b6d-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="35b6d-139">Protocol specifications</span></span>

<span data-ttu-id="35b6d-140">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35b6d-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35b6d-141">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35b6d-142">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35b6d-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35b6d-143">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="35b6d-144">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35b6d-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35b6d-145">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35b6d-146">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="35b6d-146">Header files</span></span>

<span data-ttu-id="35b6d-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35b6d-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="35b6d-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="35b6d-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="35b6d-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35b6d-149">Mapitags.h</span></span>
  
> <span data-ttu-id="35b6d-150">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35b6d-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35b6d-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="35b6d-151">See also</span></span>



[<span data-ttu-id="35b6d-152">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="35b6d-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35b6d-153">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="35b6d-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35b6d-154">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="35b6d-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35b6d-155">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="35b6d-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

