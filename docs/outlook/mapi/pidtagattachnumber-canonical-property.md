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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327252"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="e34a1-103">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e34a1-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="e34a1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e34a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e34a1-105">親メッセージ内の添付ファイルを一意に識別する番号を含みます。</span><span class="sxs-lookup"><span data-stu-id="e34a1-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e34a1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e34a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e34a1-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="e34a1-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="e34a1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e34a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e34a1-109">0x0e21</span><span class="sxs-lookup"><span data-stu-id="e34a1-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="e34a1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e34a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="e34a1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e34a1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e34a1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e34a1-112">Area:</span></span>  <br/> |<span data-ttu-id="e34a1-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="e34a1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e34a1-114">解説</span><span class="sxs-lookup"><span data-stu-id="e34a1-114">Remarks</span></span>

<span data-ttu-id="e34a1-115">メッセージストアは、このプロパティを生成して管理します。</span><span class="sxs-lookup"><span data-stu-id="e34a1-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="e34a1-116">添付ファイルの番号は、描画位置の後の2番目の並べ替えキーです (添付ファイルテーブル内)。</span><span class="sxs-lookup"><span data-stu-id="e34a1-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="e34a1-117">**PR_ATTACH_NUM**は、 [IMessage:: openattach](imessage-openattach.md)メソッドを使用して添付ファイルを開くために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e34a1-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="e34a1-118">クライアントアプリケーションのセッションでは、添付ファイルテーブルが開いている間は、メッセージの添付ファイルの**PR_ATTACH_NUM**プロパティは一定のままです。</span><span class="sxs-lookup"><span data-stu-id="e34a1-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="e34a1-119">メッセージストアは、 **IMessage:: createattach**および**IMessage::D eleteattach**メソッドを使用して、変更内容をテーブルに反映します。</span><span class="sxs-lookup"><span data-stu-id="e34a1-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="e34a1-120">このオプションでは、メッセージストアは、クライアントがそれらの変更に再同期できるように、開いている添付ファイルテーブルでテーブル通知を生成できます。</span><span class="sxs-lookup"><span data-stu-id="e34a1-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e34a1-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e34a1-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e34a1-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e34a1-122">Protocol specifications</span></span>

<span data-ttu-id="e34a1-123">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e34a1-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e34a1-124">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e34a1-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e34a1-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e34a1-125">Header files</span></span>

<span data-ttu-id="e34a1-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e34a1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e34a1-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e34a1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e34a1-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e34a1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e34a1-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e34a1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e34a1-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e34a1-130">See also</span></span>



[<span data-ttu-id="e34a1-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e34a1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e34a1-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e34a1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e34a1-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e34a1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e34a1-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e34a1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

