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
ms.openlocfilehash: 20dcef118a5e3f513f8330802684a59f0f0dcf73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565348"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="ebbad-103">PidNameContentClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebbad-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="ebbad-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebbad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebbad-105">[RFC3282] のコンテンツ クラスのヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ebbad-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebbad-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="ebbad-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ebbad-107">なし</span><span class="sxs-lookup"><span data-stu-id="ebbad-107">None</span></span>  <br/> |
|<span data-ttu-id="ebbad-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ebbad-108">Property set:</span></span>  <br/> |<span data-ttu-id="ebbad-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ebbad-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="ebbad-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="ebbad-110">Property name:</span></span>  <br/> |<span data-ttu-id="ebbad-111">コンテンツ クラス</span><span class="sxs-lookup"><span data-stu-id="ebbad-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="ebbad-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ebbad-112">Data type:</span></span>  <br/> |<span data-ttu-id="ebbad-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ebbad-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ebbad-114">領域:</span><span class="sxs-lookup"><span data-stu-id="ebbad-114">Area:</span></span>  <br/> |<span data-ttu-id="ebbad-115">メール</span><span class="sxs-lookup"><span data-stu-id="ebbad-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebbad-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ebbad-116">Remarks</span></span>

<span data-ttu-id="ebbad-117">多目的インターネット メッセージの拡張機能 (MIME) クライアントはこのプロパティの値を設定するのには、目的の値を持つコンテンツ クラスのヘッダー フィールドを記述しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ebbad-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="ebbad-118">MIME のリーダーは、このプロパティの値をコンテンツ クラスのヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebbad-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ebbad-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ebbad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebbad-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ebbad-120">Protocol specifications</span></span>

<span data-ttu-id="ebbad-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebbad-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebbad-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ebbad-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ebbad-123">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebbad-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebbad-124">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="ebbad-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ebbad-125">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebbad-125">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebbad-126">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="ebbad-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebbad-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ebbad-127">Header files</span></span>

<span data-ttu-id="ebbad-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebbad-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebbad-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ebbad-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebbad-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebbad-130">See also</span></span>



[<span data-ttu-id="ebbad-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebbad-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebbad-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebbad-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebbad-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ebbad-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebbad-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ebbad-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

