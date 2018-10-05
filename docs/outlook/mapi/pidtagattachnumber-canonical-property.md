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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401504"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="33547-103">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="33547-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="33547-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33547-105">その親メッセージ内の添付ファイルを一意に識別する番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="33547-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33547-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="33547-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33547-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="33547-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="33547-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="33547-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33547-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="33547-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="33547-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="33547-110">Data type:</span></span>  <br/> |<span data-ttu-id="33547-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33547-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33547-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="33547-112">Area:</span></span>  <br/> |<span data-ttu-id="33547-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="33547-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33547-114">備考</span><span class="sxs-lookup"><span data-stu-id="33547-114">Remarks</span></span>

<span data-ttu-id="33547-115">メッセージ ・ ストアを生成し、このプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="33547-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="33547-116">添付ファイル数が、添付ファイル テーブル内のレンダリング位置、2 番目の並べ替えキー。</span><span class="sxs-lookup"><span data-stu-id="33547-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="33547-117">[IMessage::OpenAttach](imessage-openattach.md)メソッドを使用して添付ファイルを開くには、 **PR_ATTACH_NUM**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="33547-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="33547-118">添付ファイル テーブルが開いている限り、クライアント アプリケーションのセッション内で一定のまま、メッセージの添付ファイルの**PR_ATTACH_NUM**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="33547-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="33547-119">メッセージ ・ ストアでは、 **IMessage::CreateAttach**メソッドと**IMessage::DeleteAttach**メソッドを使用して、テーブルへの変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="33547-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="33547-120">オプションで、メッセージ ・ ストアはクライアントがそれらの変更を再同期化できるように、添付ファイルを開くテーブル上のテーブルの通知を生成できます。</span><span class="sxs-lookup"><span data-stu-id="33547-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33547-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="33547-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33547-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="33547-122">Protocol specifications</span></span>

<span data-ttu-id="33547-123">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33547-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33547-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="33547-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33547-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="33547-125">Header files</span></span>

<span data-ttu-id="33547-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33547-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="33547-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="33547-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="33547-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33547-128">Mapitags.h</span></span>
  
> <span data-ttu-id="33547-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="33547-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33547-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="33547-130">See also</span></span>



[<span data-ttu-id="33547-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="33547-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33547-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="33547-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33547-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33547-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33547-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33547-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

