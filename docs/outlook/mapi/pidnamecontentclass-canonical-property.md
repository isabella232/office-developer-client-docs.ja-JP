---
title: PidNameContentClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356351"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="0b61d-103">PidNameContentClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0b61d-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="0b61d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b61d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b61d-105">[RFC3282] content-type ヘッダーフィールド値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b61d-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b61d-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="0b61d-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="0b61d-107">なし</span><span class="sxs-lookup"><span data-stu-id="0b61d-107">None</span></span>  <br/> |
|<span data-ttu-id="0b61d-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="0b61d-108">Property set:</span></span>  <br/> |<span data-ttu-id="0b61d-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="0b61d-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="0b61d-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="0b61d-110">Property name:</span></span>  <br/> |<span data-ttu-id="0b61d-111">コンテンツクラス</span><span class="sxs-lookup"><span data-stu-id="0b61d-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="0b61d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0b61d-112">Data type:</span></span>  <br/> |<span data-ttu-id="0b61d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b61d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0b61d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="0b61d-114">Area:</span></span>  <br/> |<span data-ttu-id="0b61d-115">電子メール</span><span class="sxs-lookup"><span data-stu-id="0b61d-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b61d-116">解説</span><span class="sxs-lookup"><span data-stu-id="0b61d-116">Remarks</span></span>

<span data-ttu-id="0b61d-117">このプロパティの値を設定するには、多目的インターネットメッセージ拡張機能 (MIME) クライアントで、必要な値を持つコンテンツクラスのヘッダーフィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b61d-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="0b61d-118">MIME リーダーは、コンテンツクラスのヘッダーフィールドの値をこのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b61d-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0b61d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0b61d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b61d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0b61d-120">Protocol specifications</span></span>

<span data-ttu-id="0b61d-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b61d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b61d-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b61d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b61d-123">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b61d-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b61d-124">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="0b61d-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0b61d-125">[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b61d-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b61d-126">権限が管理されたエンコード済みメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="0b61d-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b61d-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0b61d-127">Header files</span></span>

<span data-ttu-id="0b61d-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b61d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b61d-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b61d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b61d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b61d-130">See also</span></span>



[<span data-ttu-id="0b61d-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0b61d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b61d-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0b61d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b61d-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0b61d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b61d-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0b61d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

