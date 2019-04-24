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
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327448"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="28728-103">PidTagRpcOverHttpFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28728-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="28728-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28728-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28728-105">microsoft Office Outlook で、ハイパーテキスト転送プロトコル (HTTP) 経由のリモートプロシージャコール (RPC) を使用して microsoft Exchange Server に接続するために使用されるプロファイルの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="28728-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28728-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="28728-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28728-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="28728-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="28728-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="28728-108">Identifier:</span></span>  <br/> |<span data-ttu-id="28728-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="28728-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="28728-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="28728-110">Data type:</span></span>  <br/> |<span data-ttu-id="28728-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="28728-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="28728-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="28728-112">Area:</span></span>  <br/> |<span data-ttu-id="28728-113">その他</span><span class="sxs-lookup"><span data-stu-id="28728-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28728-114">解説</span><span class="sxs-lookup"><span data-stu-id="28728-114">Remarks</span></span>

<span data-ttu-id="28728-115">**PR_ROH_FLAGS**プロパティは、メッセージングアプリケーションプログラミングインターフェイス (MAPI) プロファイルの [グローバルプロファイル] セクションに格納されます。</span><span class="sxs-lookup"><span data-stu-id="28728-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="28728-116">**PR_ROH_FLAGS**の値は、次の1つ以上のフラグで構成されるビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="28728-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="28728-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="28728-117">**Name**</span></span>|<span data-ttu-id="28728-118">**値**</span><span class="sxs-lookup"><span data-stu-id="28728-118">**Value**</span></span>|<span data-ttu-id="28728-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="28728-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="28728-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="28728-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="28728-121">0x1</span><span class="sxs-lookup"><span data-stu-id="28728-121">0x1</span></span>  <br/> |<span data-ttu-id="28728-122">RPC over HTTP を使用して Exchange サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="28728-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="28728-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="28728-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="28728-124">0x2</span><span class="sxs-lookup"><span data-stu-id="28728-124">0x2</span></span>  <br/> |<span data-ttu-id="28728-125">Secure Socket Layer (SSL) のみを使用して Exchange サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="28728-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="28728-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="28728-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="28728-127">0x4</span><span class="sxs-lookup"><span data-stu-id="28728-127">0x4</span></span>  <br/> |<span data-ttu-id="28728-128">SSL を使用して接続しているときにセッションを相互認証します。</span><span class="sxs-lookup"><span data-stu-id="28728-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="28728-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="28728-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="28728-130">0x8</span><span class="sxs-lookup"><span data-stu-id="28728-130">0x8</span></span>  <br/> |<span data-ttu-id="28728-131">高速のネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="28728-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="28728-132">次に、tcp/ip を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="28728-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="28728-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="28728-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="28728-134">0x20</span><span class="sxs-lookup"><span data-stu-id="28728-134">0x20</span></span>  <br/> |<span data-ttu-id="28728-135">低速のネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="28728-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="28728-136">次に、tcp/ip を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="28728-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="28728-137">たとえば、 **PR_ROH_FLAGS**プロパティを設定して RPC over HTTP を有効にし、SSL を要求し、最初に低速接続で http プロトコルを使用するように指定するには、 **PR_ROH_FLAGS**プロパティ`ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`の値を0x23 と等しくなるように設定します。</span><span class="sxs-lookup"><span data-stu-id="28728-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="28728-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="28728-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28728-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="28728-139">Protocol specifications</span></span>

<span data-ttu-id="28728-140">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28728-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28728-141">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="28728-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28728-142">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28728-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28728-143">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="28728-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="28728-144">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28728-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28728-145">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="28728-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28728-146">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="28728-146">Header files</span></span>

<span data-ttu-id="28728-147">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28728-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="28728-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="28728-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="28728-149">Mapitags</span><span class="sxs-lookup"><span data-stu-id="28728-149">Mapitags.h</span></span>
  
> <span data-ttu-id="28728-150">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="28728-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28728-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="28728-151">See also</span></span>



[<span data-ttu-id="28728-152">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="28728-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28728-153">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28728-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28728-154">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="28728-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28728-155">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="28728-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

