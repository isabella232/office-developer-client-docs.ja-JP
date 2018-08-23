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
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802488"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="1d8d2-103">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d8d2-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="1d8d2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d8d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d8d2-105">その親メッセージ内の添付ファイルを一意に識別する番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d8d2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1d8d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d8d2-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="1d8d2-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="1d8d2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1d8d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d8d2-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="1d8d2-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="1d8d2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1d8d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d8d2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1d8d2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1d8d2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1d8d2-112">Area:</span></span>  <br/> |<span data-ttu-id="1d8d2-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="1d8d2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d8d2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1d8d2-114">Remarks</span></span>

<span data-ttu-id="1d8d2-115">メッセージ ・ ストアを生成し、このプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="1d8d2-116">添付ファイル数が、添付ファイル テーブル内のレンダリング位置、2 番目の並べ替えキー。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="1d8d2-117">[IMessage::OpenAttach](imessage-openattach.md)メソッドを使用して添付ファイルを開くには、 **PR_ATTACH_NUM**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="1d8d2-118">添付ファイル テーブルが開いている限り、クライアント アプリケーションのセッション内で一定のまま、メッセージの添付ファイルの**PR_ATTACH_NUM**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="1d8d2-119">メッセージ ・ ストアでは、 **IMessage::CreateAttach**メソッドと**IMessage::DeleteAttach**メソッドを使用して、テーブルへの変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="1d8d2-120">オプションで、メッセージ ・ ストアはクライアントがそれらの変更を再同期化できるように、添付ファイルを開くテーブル上のテーブルの通知を生成できます。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1d8d2-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1d8d2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d8d2-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1d8d2-122">Protocol specifications</span></span>

<span data-ttu-id="1d8d2-123">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d8d2-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d8d2-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d8d2-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1d8d2-125">Header files</span></span>

<span data-ttu-id="1d8d2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d8d2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d8d2-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d8d2-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d8d2-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1d8d2-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d8d2-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d8d2-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d8d2-130">See also</span></span>



[<span data-ttu-id="1d8d2-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d8d2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d8d2-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d8d2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d8d2-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1d8d2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d8d2-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1d8d2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

