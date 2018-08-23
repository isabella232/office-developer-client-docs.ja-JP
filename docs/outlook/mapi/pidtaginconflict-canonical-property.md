---
title: PidTagInConflict 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 573e0ba37d4117d85193933a3a5045b5060fbd3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802858"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="ed6f1-103">PidTagInConflict 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed6f1-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="ed6f1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed6f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed6f1-105">添付ファイルが別のレプリカを表す場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed6f1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ed6f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed6f1-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="ed6f1-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="ed6f1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ed6f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed6f1-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="ed6f1-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="ed6f1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ed6f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed6f1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ed6f1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ed6f1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ed6f1-112">Area:</span></span>  <br/> |<span data-ttu-id="ed6f1-113">競合メモ</span><span class="sxs-lookup"><span data-stu-id="ed6f1-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed6f1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ed6f1-114">Remarks</span></span>

<span data-ttu-id="ed6f1-115">電子メール クライアントとサーバーは、レプリカの同期中にメッセージの現在のバージョンとの競合を検出すると、競合解決メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="ed6f1-116">ローカルのレプリカに、メッセージの現在のバージョンが現在の同期操作中に転送されることができることを理解する重要です。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="ed6f1-117">競合既にが存在する場合、サーバー上でローカルのレプリカに矛盾したメッセージのいずれかにダウンロードされた前にこの行われます。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="ed6f1-118">競合を解決すると、メッセージが競合する Pcl を持つ独立したレプリカと同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="ed6f1-119">メッセージ自体は、クライアントとサーバー間で同期されませんする必要があります、競合の解決します。独立したレプリカのみを交換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="ed6f1-120">同期パートナーは、競合のメッセージの構造に一致する新しいメッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="ed6f1-121">したがって、クライアントとサーバーのどちらが「勝者」の項目を検出するために同じアルゴリズムを使用することがあります。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="ed6f1-122">「勝者」を検出するためには、次の規則を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="ed6f1-123">最終変更時刻です。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-123">Last modification time.</span></span>
    
2. <span data-ttu-id="ed6f1-124">(メモリの比較を使用して) 以上の CN GUID リンク付けを解除します。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ed6f1-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ed6f1-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed6f1-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ed6f1-126">Protocol specifications</span></span>

<span data-ttu-id="ed6f1-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed6f1-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed6f1-128">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed6f1-129">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed6f1-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed6f1-130">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed6f1-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ed6f1-131">Header files</span></span>

<span data-ttu-id="ed6f1-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed6f1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed6f1-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed6f1-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed6f1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="ed6f1-135">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed6f1-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed6f1-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed6f1-136">See also</span></span>



[<span data-ttu-id="ed6f1-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed6f1-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed6f1-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed6f1-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed6f1-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ed6f1-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed6f1-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ed6f1-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

