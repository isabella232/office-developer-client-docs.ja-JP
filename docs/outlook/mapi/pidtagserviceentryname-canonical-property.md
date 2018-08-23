---
title: PidTagServiceEntryName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3988596cc0b9c01d526354dabef3a6e7fdefc3b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583226"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="4f862-103">PidTagServiceEntryName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f862-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="4f862-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f862-105">メッセージ サービスの構成のエントリ ポイント関数の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f862-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f862-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4f862-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f862-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="4f862-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="4f862-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4f862-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f862-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="4f862-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="4f862-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4f862-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f862-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4f862-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4f862-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4f862-112">Area:</span></span>  <br/> |<span data-ttu-id="4f862-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="4f862-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f862-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4f862-114">Remarks</span></span>

<span data-ttu-id="4f862-115">メッセージ サービスのエントリ ポイントを提供するメッセージ サービスの実装者が、エントリ ポイントが必要ではないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4f862-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="4f862-116">ただし、エントリ ポイントは、関連する設定のプロパティが存在する場合にのみ指定してください。</span><span class="sxs-lookup"><span data-stu-id="4f862-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="4f862-117">MAPI ではこれらのプロパティが存在しない場合、エントリ ポイントが指定されていないと見なされます。</span><span class="sxs-lookup"><span data-stu-id="4f862-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="4f862-118">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) は、エントリ ポイント関数が入力されているダイナミック リンク ライブラリ (DLL) と呼びます。</span><span class="sxs-lookup"><span data-stu-id="4f862-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="4f862-119">メッセージ サービスのエントリ ポイントの詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f862-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f862-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4f862-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4f862-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4f862-121">Header files</span></span>

<span data-ttu-id="4f862-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f862-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f862-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f862-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f862-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f862-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4f862-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f862-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f862-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f862-126">See also</span></span>



[<span data-ttu-id="4f862-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f862-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f862-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f862-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f862-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f862-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f862-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f862-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

