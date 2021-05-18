---
title: PidTagViewDescriptorName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360726"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a><span data-ttu-id="a9f96-103">PidTagViewDescriptorName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9f96-103">PidTagViewDescriptorName Canonical Property</span></span>

  
  
<span data-ttu-id="a9f96-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9f96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9f96-105">ビュー記述子の名前が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a9f96-105">Contains the name of a view descriptor.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9f96-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a9f96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9f96-107">PR_VD_NAME、PR_VD_NAME_A、PR_VD_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a9f96-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a9f96-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a9f96-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9f96-109">0x7006</span><span class="sxs-lookup"><span data-stu-id="a9f96-109">0x7006</span></span>  <br/> |
|<span data-ttu-id="a9f96-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a9f96-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9f96-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9f96-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9f96-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a9f96-112">Area:</span></span>  <br/> |<span data-ttu-id="a9f96-113">メッセージ クラス定義の送信可能</span><span class="sxs-lookup"><span data-stu-id="a9f96-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9f96-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a9f96-114">Remarks</span></span>

<span data-ttu-id="a9f96-115">これらのプロパティは、ビュー定義を含むフォルダー関連情報 (FAI) メッセージの空でない文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9f96-115">These properties must be set to a non-empty string for a Folder Associate Information (FAI) message that contains view definitions.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9f96-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a9f96-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9f96-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a9f96-117">Protocol specifications</span></span>

<span data-ttu-id="a9f96-118">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9f96-118">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9f96-119">共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a9f96-119">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9f96-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a9f96-120">Header files</span></span>

<span data-ttu-id="a9f96-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9f96-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9f96-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9f96-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9f96-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9f96-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a9f96-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a9f96-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9f96-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9f96-125">See also</span></span>



[<span data-ttu-id="a9f96-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a9f96-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9f96-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9f96-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9f96-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a9f96-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9f96-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a9f96-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

