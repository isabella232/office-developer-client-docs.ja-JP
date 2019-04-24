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
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358535"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="5099a-103">PidTagInConflict 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5099a-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="5099a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5099a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5099a-105">添付ファイルが代替レプリカを表す場合は TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5099a-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5099a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5099a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5099a-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="5099a-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="5099a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5099a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5099a-109">0x666c</span><span class="sxs-lookup"><span data-stu-id="5099a-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="5099a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5099a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5099a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5099a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5099a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5099a-112">Area:</span></span>  <br/> |<span data-ttu-id="5099a-113">競合メモ</span><span class="sxs-lookup"><span data-stu-id="5099a-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5099a-114">解説</span><span class="sxs-lookup"><span data-stu-id="5099a-114">Remarks</span></span>

<span data-ttu-id="5099a-115">同期中にレプリカ内のメッセージの現在のバージョンに対して競合を検出する場合、電子メールクライアントとサーバーは競合の解決メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5099a-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="5099a-116">現在の同期操作中にローカルレプリカ内のメッセージの現在のバージョンが転送された可能性があることを理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="5099a-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="5099a-117">これは、競合しているメッセージがローカルレプリカにダウンロードされる前に、サーバー上に競合が既に存在する場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="5099a-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="5099a-118">競合を解決するメッセージは、pcls が競合している独立したレプリカとして同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5099a-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="5099a-119">競合を解決するメッセージ自体は、クライアントとサーバーの間で同期してはなりません。独立したレプリカのみを交換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5099a-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="5099a-120">同期パートナーは、競合メッセージの構造に一致する新しいメッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5099a-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="5099a-121">そのため、クライアントとサーバーが同じアルゴリズムを使用して "勝者" アイテムを検出することが重要です。</span><span class="sxs-lookup"><span data-stu-id="5099a-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="5099a-122">"勝者" を検出するには、次のルールを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5099a-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="5099a-123">最終変更日時。</span><span class="sxs-lookup"><span data-stu-id="5099a-123">Last modification time.</span></span>
    
2. <span data-ttu-id="5099a-124">関連付けを解除するために、より高い CN GUID (メモリ比較を使用)。</span><span class="sxs-lookup"><span data-stu-id="5099a-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5099a-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5099a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5099a-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5099a-126">Protocol specifications</span></span>

<span data-ttu-id="5099a-127">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5099a-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5099a-128">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5099a-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5099a-129">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5099a-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5099a-130">サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="5099a-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5099a-131">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5099a-131">Header files</span></span>

<span data-ttu-id="5099a-132">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5099a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="5099a-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5099a-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="5099a-134">Mapitags</span><span class="sxs-lookup"><span data-stu-id="5099a-134">Mapitags.h</span></span>
  
> <span data-ttu-id="5099a-135">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5099a-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5099a-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="5099a-136">See also</span></span>



[<span data-ttu-id="5099a-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5099a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5099a-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5099a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5099a-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5099a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5099a-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5099a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

