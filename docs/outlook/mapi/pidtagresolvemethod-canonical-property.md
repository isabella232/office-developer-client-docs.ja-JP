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
ms.openlocfilehash: 7f55b85e21f007be7c1b9d42d42473e3a8d2becb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803361"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="ec9ca-103">PidTagResolveMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec9ca-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="ec9ca-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec9ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec9ca-105">フォルダーの競合の解像度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec9ca-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ec9ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec9ca-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="ec9ca-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="ec9ca-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ec9ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec9ca-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="ec9ca-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="ec9ca-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ec9ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec9ca-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ec9ca-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ec9ca-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ec9ca-112">Area:</span></span>  <br/> |<span data-ttu-id="ec9ca-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="ec9ca-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec9ca-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ec9ca-114">Remarks</span></span>

<span data-ttu-id="ec9ca-115">競合解決メッセージを含むフォルダーでこのプロパティは、競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="ec9ca-116">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-116">This property is not required.</span></span> <span data-ttu-id="ec9ca-117">ただし、設定されている場合以外の次のフラグする必要がありますは使用されません。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec9ca-118">RESOLVE_METHOD_DEFAULT (0X00000000)</span><span class="sxs-lookup"><span data-stu-id="ec9ca-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="ec9ca-119">競合を解決すると、メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="ec9ca-120">RESOLVE_METHOD_LAST_WRITER_WINS (0X00000001)</span><span class="sxs-lookup"><span data-stu-id="ec9ca-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="ec9ca-121">現在の変更を適用する対象のメッセージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="ec9ca-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0X00000002)</span><span class="sxs-lookup"><span data-stu-id="ec9ca-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="ec9ca-123">パブリック フォルダー内のメッセージを解決する競合を生成するときに競合の通知メッセージを送信しません。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="ec9ca-124">クライアントまたはサーバーする必要があります競合解決メッセージが関連付けられているメッセージを生成することができません。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="ec9ca-125">**RESOLVE_METHOD_LAST_WRITER_WINS**セマンティクスを使用してこれらのメッセージを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ec9ca-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ec9ca-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec9ca-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ec9ca-127">Protocol specifications</span></span>

<span data-ttu-id="ec9ca-128">[[MS OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec9ca-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec9ca-129">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="ec9ca-130">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec9ca-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec9ca-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec9ca-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ec9ca-132">Header files</span></span>

<span data-ttu-id="ec9ca-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec9ca-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec9ca-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec9ca-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec9ca-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ec9ca-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec9ca-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec9ca-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec9ca-137">See also</span></span>



[<span data-ttu-id="ec9ca-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec9ca-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec9ca-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec9ca-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec9ca-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ec9ca-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec9ca-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ec9ca-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

