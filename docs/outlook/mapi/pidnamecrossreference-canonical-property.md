---
title: PidNameCrossReference 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331445"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="19894-103">PidNameCrossReference 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19894-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="19894-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19894-105">[RFC3282] Xref ヘッダーフィールド値を含みます。</span><span class="sxs-lookup"><span data-stu-id="19894-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19894-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="19894-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="19894-107">なし</span><span class="sxs-lookup"><span data-stu-id="19894-107">None</span></span>  <br/> |
|<span data-ttu-id="19894-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="19894-108">Property set:</span></span>  <br/> |<span data-ttu-id="19894-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="19894-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="19894-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="19894-110">Property name:</span></span>  <br/> |<span data-ttu-id="19894-111">相互</span><span class="sxs-lookup"><span data-stu-id="19894-111">Xref</span></span>  <br/> |
|<span data-ttu-id="19894-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="19894-112">Data type:</span></span>  <br/> |<span data-ttu-id="19894-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="19894-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="19894-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="19894-114">Area:</span></span>  <br/> |<span data-ttu-id="19894-115">電子メール</span><span class="sxs-lookup"><span data-stu-id="19894-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19894-116">解説</span><span class="sxs-lookup"><span data-stu-id="19894-116">Remarks</span></span>

<span data-ttu-id="19894-117">このプロパティの値を設定するには、多目的のインターネットメッセージ拡張機能 (MIME) クライアントで、必要な値を XRef ヘッダーフィールドに書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="19894-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="19894-118">MIME リーダーは、XRef ヘッダーフィールドの値をこのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="19894-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="19894-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="19894-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19894-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="19894-120">Protocol specifications</span></span>

<span data-ttu-id="19894-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19894-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19894-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="19894-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19894-123">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19894-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19894-124">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="19894-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19894-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="19894-125">Header files</span></span>

<span data-ttu-id="19894-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19894-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="19894-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="19894-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19894-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="19894-128">See also</span></span>



[<span data-ttu-id="19894-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="19894-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19894-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19894-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19894-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="19894-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19894-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="19894-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

