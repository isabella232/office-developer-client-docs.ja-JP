---
title: PidTagReportSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 889b43bb606cbe9c96d52c8a21ffda5dfcebb1da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359179"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="47946-103">PidTagReportSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47946-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="47946-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47946-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47946-105">このメッセージのレポートを取得する受信者の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="47946-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47946-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47946-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47946-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="47946-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="47946-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="47946-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47946-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="47946-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="47946-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47946-110">Data type:</span></span>  <br/> |<span data-ttu-id="47946-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="47946-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="47946-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="47946-112">Area:</span></span>  <br/> |<span data-ttu-id="47946-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="47946-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47946-114">解説</span><span class="sxs-lookup"><span data-stu-id="47946-114">Remarks</span></span>

<span data-ttu-id="47946-115">このプロパティは、このメッセージに対して生成されたすべてのレポートを送信者が受信することを送信者が委任した、受信者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="47946-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="47946-116">他のユーザーにレポートをルーティングする必要があるクライアントアプリケーションは、メッセージ送信時にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47946-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="47946-117">設定されていない場合、レポートはメッセージ送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="47946-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47946-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47946-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47946-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47946-119">Protocol specifications</span></span>

<span data-ttu-id="47946-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47946-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47946-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="47946-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47946-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47946-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47946-123">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47946-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47946-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="47946-124">Header files</span></span>

<span data-ttu-id="47946-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47946-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="47946-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47946-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="47946-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="47946-127">Mapitags.h</span></span>
  
> <span data-ttu-id="47946-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47946-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47946-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="47946-129">See also</span></span>



[<span data-ttu-id="47946-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="47946-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47946-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47946-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47946-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47946-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47946-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47946-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

