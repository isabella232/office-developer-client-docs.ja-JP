---
title: PidTagViewsEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 73ed7213ea2bd5079458ccc237b65590f06e8d53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586264"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="c1c11-103">PidTagViewsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1c11-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c1c11-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1c11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1c11-105">ユーザー定義ビュー] フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1c11-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1c11-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c1c11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1c11-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c1c11-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c1c11-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c1c11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1c11-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="c1c11-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="c1c11-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c1c11-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1c11-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c1c11-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c1c11-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c1c11-112">Area:</span></span>  <br/> |<span data-ttu-id="c1c11-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="c1c11-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1c11-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c1c11-114">Remarks</span></span>

<span data-ttu-id="c1c11-115">共通のフォルダー ビューにはには、フォルダーのビューには、メッセージングのユーザーによって定義された指定子が含まれているときに標準のビューの指定子の定義済みセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1c11-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="c1c11-116">表示指定子が多く、各メッセージとして格納されているこれらのフォルダーは、個人間メッセージ (IPM) の階層構造で表示されていないを保持できます。</span><span class="sxs-lookup"><span data-stu-id="c1c11-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="c1c11-117">指定子のセットの 2 つをマージして両方使用できるようにするクライアント アプリケーションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c1c11-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c1c11-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c1c11-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c1c11-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c1c11-119">Header files</span></span>

<span data-ttu-id="c1c11-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1c11-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1c11-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1c11-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1c11-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c1c11-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c1c11-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1c11-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1c11-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1c11-124">See also</span></span>



[<span data-ttu-id="c1c11-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1c11-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1c11-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1c11-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1c11-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1c11-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1c11-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1c11-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

