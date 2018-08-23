---
title: PidTagReportName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803346"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="2e769-103">PidTagReportName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e769-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="2e769-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e769-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e769-105">このメッセージのレポートを取得する必要があります受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e769-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e769-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2e769-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e769-107">PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2e769-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2e769-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2e769-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e769-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="2e769-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="2e769-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2e769-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e769-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e769-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e769-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2e769-112">Area:</span></span>  <br/> |<span data-ttu-id="2e769-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="2e769-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e769-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2e769-114">Remarks</span></span>

<span data-ttu-id="2e769-115">これらのプロパティでは、このメッセージに対して生成されたすべてのレポートを受信する送信者を委任した受信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="2e769-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="2e769-116">レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e769-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="2e769-117">設定されていない場合、レポートは、メッセージの送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2e769-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e769-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2e769-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e769-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2e769-119">Header files</span></span>

<span data-ttu-id="2e769-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e769-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e769-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e769-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e769-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e769-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2e769-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e769-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e769-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e769-124">See also</span></span>



[<span data-ttu-id="2e769-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e769-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e769-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e769-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e769-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2e769-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e769-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2e769-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

