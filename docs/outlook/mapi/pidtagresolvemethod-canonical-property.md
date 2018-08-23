---
title: PidTagResolveMethod 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e67cbb113899487f489ef7235d92d1adfcb76163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563640"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="ca338-103">PidTagResolveMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca338-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="ca338-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca338-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca338-105">フォルダーの競合の解像度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca338-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca338-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ca338-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca338-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="ca338-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="ca338-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ca338-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca338-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="ca338-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="ca338-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ca338-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca338-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ca338-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ca338-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ca338-112">Area:</span></span>  <br/> |<span data-ttu-id="ca338-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="ca338-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca338-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ca338-114">Remarks</span></span>

<span data-ttu-id="ca338-115">競合解決メッセージを含むフォルダーでこのプロパティは、競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ca338-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="ca338-116">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="ca338-116">This property is not required.</span></span> <span data-ttu-id="ca338-117">ただし、設定されている場合以外の次のフラグする必要がありますは使用されません。</span><span class="sxs-lookup"><span data-stu-id="ca338-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca338-118">RESOLVE_METHOD_DEFAULT (0X00000000)</span><span class="sxs-lookup"><span data-stu-id="ca338-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="ca338-119">競合を解決すると、メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca338-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="ca338-120">RESOLVE_METHOD_LAST_WRITER_WINS (0X00000001)</span><span class="sxs-lookup"><span data-stu-id="ca338-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="ca338-121">現在の変更を適用する対象のメッセージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ca338-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="ca338-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0X00000002)</span><span class="sxs-lookup"><span data-stu-id="ca338-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="ca338-123">パブリック フォルダー内のメッセージを解決する競合を生成するときに競合の通知メッセージを送信しません。</span><span class="sxs-lookup"><span data-stu-id="ca338-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="ca338-124">クライアントまたはサーバーする必要があります競合解決メッセージが関連付けられているメッセージを生成することができません。</span><span class="sxs-lookup"><span data-stu-id="ca338-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="ca338-125">**RESOLVE_METHOD_LAST_WRITER_WINS**セマンティクスを使用してこれらのメッセージを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca338-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ca338-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ca338-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca338-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ca338-127">Protocol specifications</span></span>

<span data-ttu-id="ca338-128">[[MS OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca338-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca338-129">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="ca338-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="ca338-130">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca338-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca338-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="ca338-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca338-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ca338-132">Header files</span></span>

<span data-ttu-id="ca338-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca338-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca338-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca338-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca338-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca338-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ca338-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca338-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca338-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca338-137">See also</span></span>



[<span data-ttu-id="ca338-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca338-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca338-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca338-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca338-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca338-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca338-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca338-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

