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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a186af55a8a2846bbb8af9e51be45ef73ce5d66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803662"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a><span data-ttu-id="bfb37-103">PidTagViewDescriptorName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bfb37-103">PidTagViewDescriptorName Canonical Property</span></span>

  
  
<span data-ttu-id="bfb37-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfb37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfb37-105">ビュー記述子の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bfb37-105">Contains the name of a view descriptor.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfb37-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bfb37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfb37-107">PR_VD_NAME、PR_VD_NAME_A、PR_VD_NAME_W</span><span class="sxs-lookup"><span data-stu-id="bfb37-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span></span>  <br/> |
|<span data-ttu-id="bfb37-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bfb37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfb37-109">0x7006</span><span class="sxs-lookup"><span data-stu-id="bfb37-109">0x7006</span></span>  <br/> |
|<span data-ttu-id="bfb37-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bfb37-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfb37-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bfb37-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bfb37-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bfb37-112">Area:</span></span>  <br/> |<span data-ttu-id="bfb37-113">クラスによって定義されたメッセージ送信できます。</span><span class="sxs-lookup"><span data-stu-id="bfb37-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfb37-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bfb37-114">Remarks</span></span>

<span data-ttu-id="bfb37-115">これらのプロパティは、ビューの定義を含むフォルダーに関連付ける情報 (FAI) メッセージの空でない文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfb37-115">These properties must be set to a non-empty string for a Folder Associate Information (FAI) message that contains view definitions.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bfb37-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bfb37-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfb37-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bfb37-117">Protocol specifications</span></span>

<span data-ttu-id="bfb37-118">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfb37-118">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfb37-119">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="bfb37-119">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfb37-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bfb37-120">Header files</span></span>

<span data-ttu-id="bfb37-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfb37-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfb37-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bfb37-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfb37-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bfb37-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bfb37-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bfb37-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfb37-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="bfb37-125">See also</span></span>



[<span data-ttu-id="bfb37-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bfb37-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfb37-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bfb37-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfb37-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bfb37-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfb37-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bfb37-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

