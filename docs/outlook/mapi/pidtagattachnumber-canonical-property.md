---
title: PidTagAttachNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327252"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="abea9-103">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="abea9-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="abea9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abea9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abea9-105">親メッセージ内の添付ファイルを一意に識別する番号を含む。</span><span class="sxs-lookup"><span data-stu-id="abea9-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abea9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="abea9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abea9-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="abea9-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="abea9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="abea9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="abea9-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="abea9-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="abea9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="abea9-110">Data type:</span></span>  <br/> |<span data-ttu-id="abea9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="abea9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="abea9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="abea9-112">Area:</span></span>  <br/> |<span data-ttu-id="abea9-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="abea9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abea9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="abea9-114">Remarks</span></span>

<span data-ttu-id="abea9-115">メッセージ ストアは、このプロパティを生成および管理します。</span><span class="sxs-lookup"><span data-stu-id="abea9-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="abea9-116">添付ファイル番号は、添付ファイル テーブルのレンダリング位置の後のセカンダリ 並べ替えキーです。</span><span class="sxs-lookup"><span data-stu-id="abea9-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="abea9-117">**PR_ATTACH_NUM** は [、IMessage::OpenAttach](imessage-openattach.md) メソッドを使用して添付ファイルを開くのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="abea9-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="abea9-118">クライアント アプリケーションのセッション内では、PR_ATTACH_NUM **テーブルが** 開いている限り、メッセージ添付ファイルのプロパティは一定のままです。</span><span class="sxs-lookup"><span data-stu-id="abea9-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="abea9-119">メッセージ ストアは **、IMessage::CreateAttach** メソッドと **IMessage::D eleteAttach** メソッドを使用してテーブルに変更を伝達します。</span><span class="sxs-lookup"><span data-stu-id="abea9-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="abea9-120">そのオプションで、メッセージ ストアは開いている添付ファイル テーブルにテーブル通知を生成して、クライアントがそれらの変更に再同期できます。</span><span class="sxs-lookup"><span data-stu-id="abea9-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="abea9-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="abea9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abea9-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="abea9-122">Protocol specifications</span></span>

<span data-ttu-id="abea9-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abea9-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abea9-124">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="abea9-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abea9-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="abea9-125">Header files</span></span>

<span data-ttu-id="abea9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abea9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="abea9-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="abea9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="abea9-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="abea9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="abea9-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="abea9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abea9-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="abea9-130">See also</span></span>



[<span data-ttu-id="abea9-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="abea9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abea9-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="abea9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abea9-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="abea9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abea9-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="abea9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

