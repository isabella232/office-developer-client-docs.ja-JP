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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331403"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="52af8-103">PidTagResolveMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="52af8-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="52af8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52af8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52af8-105">フォルダーの競合解決の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="52af8-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52af8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="52af8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52af8-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="52af8-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="52af8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="52af8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52af8-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="52af8-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="52af8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="52af8-110">Data type:</span></span>  <br/> |<span data-ttu-id="52af8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="52af8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="52af8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="52af8-112">Area:</span></span>  <br/> |<span data-ttu-id="52af8-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="52af8-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52af8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="52af8-114">Remarks</span></span>

<span data-ttu-id="52af8-115">競合解決メッセージを含むフォルダーのこのプロパティは、競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="52af8-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="52af8-116">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="52af8-116">This property is not required.</span></span> <span data-ttu-id="52af8-117">ただし、設定されている場合は、次以外のフラグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52af8-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52af8-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="52af8-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="52af8-119">競合解決メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52af8-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="52af8-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="52af8-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="52af8-121">現在の変更が適用されているターゲット メッセージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="52af8-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="52af8-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="52af8-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="52af8-123">パブリック フォルダーで競合解決メッセージを生成するときに、競合通知メッセージを送信しない。</span><span class="sxs-lookup"><span data-stu-id="52af8-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="52af8-124">クライアントまたはサーバーは、関連付けられたメッセージに対して競合解決メッセージを生成しなける必要があります。</span><span class="sxs-lookup"><span data-stu-id="52af8-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="52af8-125">これらのメッセージは、次のセマンティクスを使用 **RESOLVE_METHOD_LAST_WRITER_WINS** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="52af8-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52af8-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="52af8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52af8-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="52af8-127">Protocol specifications</span></span>

<span data-ttu-id="52af8-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52af8-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52af8-129">サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="52af8-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="52af8-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52af8-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52af8-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="52af8-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52af8-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="52af8-132">Header files</span></span>

<span data-ttu-id="52af8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52af8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="52af8-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="52af8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="52af8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52af8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="52af8-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="52af8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52af8-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="52af8-137">See also</span></span>



[<span data-ttu-id="52af8-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="52af8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52af8-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="52af8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52af8-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="52af8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52af8-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="52af8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

