---
title: PidTagExpiryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316374"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="965c0-103">PidTagExpiryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="965c0-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="965c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="965c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="965c0-105">メッセージングシステムがメッセージの内容を無効にできる日時を含みます。</span><span class="sxs-lookup"><span data-stu-id="965c0-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="965c0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="965c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="965c0-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="965c0-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="965c0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="965c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="965c0-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="965c0-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="965c0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="965c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="965c0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="965c0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="965c0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="965c0-112">Area:</span></span>  <br/> |<span data-ttu-id="965c0-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="965c0-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="965c0-114">解説</span><span class="sxs-lookup"><span data-stu-id="965c0-114">Remarks</span></span>

<span data-ttu-id="965c0-115">このプロパティは、配信された個人間メッセージを処理するようにメッセージングシステムを指示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="965c0-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="965c0-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="965c0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="965c0-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="965c0-117">Protocol specifications</span></span>

<span data-ttu-id="965c0-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="965c0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="965c0-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="965c0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="965c0-120">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="965c0-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="965c0-121">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="965c0-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="965c0-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="965c0-122">Header files</span></span>

<span data-ttu-id="965c0-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="965c0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="965c0-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="965c0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="965c0-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="965c0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="965c0-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="965c0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="965c0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="965c0-127">See also</span></span>



[<span data-ttu-id="965c0-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="965c0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="965c0-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="965c0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="965c0-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="965c0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="965c0-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="965c0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

