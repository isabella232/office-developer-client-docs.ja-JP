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
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331403"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="6647e-103">PidTagResolveMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6647e-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="6647e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6647e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6647e-105">フォルダーの競合の解決の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6647e-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6647e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6647e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6647e-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="6647e-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="6647e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6647e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6647e-109">0x3fe7</span><span class="sxs-lookup"><span data-stu-id="6647e-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="6647e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6647e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6647e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6647e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6647e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6647e-112">Area:</span></span>  <br/> |<span data-ttu-id="6647e-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="6647e-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6647e-114">解説</span><span class="sxs-lookup"><span data-stu-id="6647e-114">Remarks</span></span>

<span data-ttu-id="6647e-115">競合の解決方法を含むフォルダーでこのプロパティを指定すると、競合を解決する方法が示されます。</span><span class="sxs-lookup"><span data-stu-id="6647e-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="6647e-116">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="6647e-116">This property is not required.</span></span> <span data-ttu-id="6647e-117">ただし、これが設定されている場合は、次のようなフラグは存在しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="6647e-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6647e-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="6647e-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="6647e-119">競合解決メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6647e-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="6647e-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6647e-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="6647e-121">ターゲットメッセージを上書きして、現在の変更が適用されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="6647e-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="6647e-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="6647e-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="6647e-123">パブリックフォルダーで競合の解決メッセージを生成するときに、競合の通知メッセージを送信しません。</span><span class="sxs-lookup"><span data-stu-id="6647e-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="6647e-124">クライアントまたはサーバーは、関連付けられたメッセージに対して競合の解決メッセージを生成してはなりません。</span><span class="sxs-lookup"><span data-stu-id="6647e-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="6647e-125">これらのメッセージは、 **RESOLVE_METHOD_LAST_WRITER_WINS**語義を使用して解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6647e-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6647e-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6647e-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6647e-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6647e-127">Protocol specifications</span></span>

<span data-ttu-id="6647e-128">[[OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6647e-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6647e-129">サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="6647e-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="6647e-130">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6647e-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6647e-131">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="6647e-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6647e-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6647e-132">Header files</span></span>

<span data-ttu-id="6647e-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6647e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="6647e-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6647e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="6647e-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="6647e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="6647e-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6647e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6647e-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="6647e-137">See also</span></span>



[<span data-ttu-id="6647e-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6647e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6647e-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6647e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6647e-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6647e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6647e-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6647e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

