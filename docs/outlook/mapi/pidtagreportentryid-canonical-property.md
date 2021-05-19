---
title: PidTagReportEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b4432650d5c9fc77c4db0bc9aed4234d85e7fdf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346320"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="75cc9-103">PidTagReportEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75cc9-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="75cc9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75cc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75cc9-105">このメッセージのレポートを受信する受信者のエントリ識別子を含む。</span><span class="sxs-lookup"><span data-stu-id="75cc9-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75cc9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="75cc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75cc9-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="75cc9-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="75cc9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="75cc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75cc9-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="75cc9-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="75cc9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="75cc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="75cc9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75cc9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="75cc9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="75cc9-112">Area:</span></span>  <br/> |<span data-ttu-id="75cc9-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="75cc9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75cc9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="75cc9-114">Remarks</span></span>

<span data-ttu-id="75cc9-115">このプロパティは、送信者がこのメッセージに対して生成されたレポートを受信するために委任した受信者のアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="75cc9-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="75cc9-116">レポートを別のユーザーにルーティングする必要があるクライアント アプリケーションは、メッセージの送信時にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75cc9-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="75cc9-117">設定されていない場合、レポートはメッセージ送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="75cc9-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75cc9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="75cc9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75cc9-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="75cc9-119">Protocol specifications</span></span>

<span data-ttu-id="75cc9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75cc9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75cc9-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="75cc9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75cc9-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75cc9-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75cc9-123">電子メール メッセージで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="75cc9-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75cc9-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="75cc9-124">Header files</span></span>

<span data-ttu-id="75cc9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75cc9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="75cc9-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="75cc9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="75cc9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75cc9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="75cc9-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="75cc9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75cc9-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="75cc9-129">See also</span></span>



[<span data-ttu-id="75cc9-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="75cc9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75cc9-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75cc9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75cc9-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="75cc9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75cc9-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="75cc9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

