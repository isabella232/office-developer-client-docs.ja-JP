---
title: PidTagRpcOverHttpFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803366"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="5bcea-103">PidTagRpcOverHttpFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5bcea-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5bcea-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bcea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bcea-105">ハイパー テキスト転送プロトコル (HTTP) 経由でリモート プロシージャ コール (RPC) を使用して Microsoft Exchange Server に接続する Microsoft Office Outlook で使用されるプロファイルの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5bcea-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bcea-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5bcea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bcea-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5bcea-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5bcea-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5bcea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5bcea-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="5bcea-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="5bcea-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-110">Data type:</span></span>  <br/> |<span data-ttu-id="5bcea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5bcea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5bcea-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5bcea-112">Area:</span></span>  <br/> |<span data-ttu-id="5bcea-113">その他</span><span class="sxs-lookup"><span data-stu-id="5bcea-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bcea-114">備考</span><span class="sxs-lookup"><span data-stu-id="5bcea-114">Remarks</span></span>

<span data-ttu-id="5bcea-115">**PR_ROH_FLAGS**プロパティは、メッセージング アプリケーション プログラミング インターフェイス (MAPI) プロファイルのグローバル プロファイル セクションに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5bcea-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="5bcea-116">**PR_ROH_FLAGS**の値は、次のフラグの 1 つ以上で構成されるビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5bcea-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="5bcea-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="5bcea-117">**Name**</span></span>|<span data-ttu-id="5bcea-118">**値**</span><span class="sxs-lookup"><span data-stu-id="5bcea-118">**Value**</span></span>|<span data-ttu-id="5bcea-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5bcea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bcea-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="5bcea-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="5bcea-121">0x1</span><span class="sxs-lookup"><span data-stu-id="5bcea-121">0x1</span></span>  <br/> |<span data-ttu-id="5bcea-122">HTTP 経由で RPC を使用して Exchange Server に接続します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="5bcea-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="5bcea-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="5bcea-124">0x2</span><span class="sxs-lookup"><span data-stu-id="5bcea-124">0x2</span></span>  <br/> |<span data-ttu-id="5bcea-125">セキュア ソケット レイヤー (SSL) のみを使用して Exchange Server に接続します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="5bcea-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="5bcea-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="5bcea-127">0x4</span><span class="sxs-lookup"><span data-stu-id="5bcea-127">0x4</span></span>  <br/> |<span data-ttu-id="5bcea-128">セッションを相互認証で SSL を使用して接続するとき。</span><span class="sxs-lookup"><span data-stu-id="5bcea-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="5bcea-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="5bcea-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="5bcea-130">0x8</span><span class="sxs-lookup"><span data-stu-id="5bcea-130">0x8</span></span>  <br/> |<span data-ttu-id="5bcea-131">高速ネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="5bcea-132">TCP/IP を使用して接続し、します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="5bcea-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="5bcea-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="5bcea-134">0x20</span><span class="sxs-lookup"><span data-stu-id="5bcea-134">0x20</span></span>  <br/> |<span data-ttu-id="5bcea-135">低速ネットワークでは、最初に HTTP を使用して接続します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="5bcea-136">TCP/IP を使用して接続し、します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="5bcea-137">たとえば、 **PR_ROH_FLAGS**を設定するのにを RPC over HTTP、SSL を要求して、低速接続で HTTP プロトコルを最初に使用することを指定する有効にするプロパティの値を設定、 **PR_ROH_FLAGS**プロパティを`ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`0x23 に等しいであります。</span><span class="sxs-lookup"><span data-stu-id="5bcea-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5bcea-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5bcea-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bcea-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5bcea-139">Protocol specifications</span></span>

<span data-ttu-id="5bcea-140">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bcea-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bcea-141">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5bcea-142">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bcea-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bcea-143">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="5bcea-144">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bcea-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bcea-145">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bcea-146">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5bcea-146">Header files</span></span>

<span data-ttu-id="5bcea-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bcea-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bcea-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5bcea-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="5bcea-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5bcea-149">Mapitags.h</span></span>
  
> <span data-ttu-id="5bcea-150">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5bcea-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bcea-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bcea-151">See also</span></span>



[<span data-ttu-id="5bcea-152">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bcea-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bcea-153">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bcea-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bcea-154">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5bcea-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bcea-155">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5bcea-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

