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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427312"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="f9ffc-103">PidTagViewsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f9ffc-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f9ffc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9ffc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9ffc-105">ユーザー定義の Views フォルダーのエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="f9ffc-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9ffc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f9ffc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9ffc-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f9ffc-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f9ffc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f9ffc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9ffc-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="f9ffc-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="f9ffc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f9ffc-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9ffc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f9ffc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f9ffc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f9ffc-112">Area:</span></span>  <br/> |<span data-ttu-id="f9ffc-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="f9ffc-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9ffc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f9ffc-114">Remarks</span></span>

<span data-ttu-id="f9ffc-115">共通ビュー フォルダーには定義済みの標準ビュー指定子のセットが含まれる一方、ビュー フォルダーにはメッセージング ユーザーによって定義された指定子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f9ffc-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="f9ffc-116">これらのフォルダーは、対人間メッセージ (IPM) 階層には表示されませんが、多くのビュー指定子を保持できます。各フォルダーはメッセージとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="f9ffc-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="f9ffc-117">クライアント アプリケーションでは、2 つの指定子セットを結合し、両方を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f9ffc-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f9ffc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f9ffc-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f9ffc-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f9ffc-119">Header files</span></span>

<span data-ttu-id="f9ffc-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9ffc-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9ffc-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f9ffc-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9ffc-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f9ffc-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f9ffc-123">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f9ffc-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9ffc-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9ffc-124">See also</span></span>



[<span data-ttu-id="f9ffc-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f9ffc-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9ffc-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f9ffc-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9ffc-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f9ffc-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9ffc-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f9ffc-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

