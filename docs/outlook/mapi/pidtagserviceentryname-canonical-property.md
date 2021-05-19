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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432472"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="2e159-103">PidTagServiceEntryName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e159-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="2e159-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e159-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e159-105">メッセージ サービスの構成用のエントリ ポイント関数の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="2e159-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e159-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2e159-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e159-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="2e159-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="2e159-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2e159-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e159-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="2e159-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="2e159-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2e159-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e159-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2e159-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="2e159-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2e159-112">Area:</span></span>  <br/> |<span data-ttu-id="2e159-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="2e159-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e159-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2e159-114">Remarks</span></span>

<span data-ttu-id="2e159-115">メッセージ サービスの実装者は、メッセージ サービスエントリ ポイントを提供しますが、エントリ ポイントは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2e159-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="2e159-116">ただし、エントリ ポイントは、関連する構成プロパティが存在する場合にのみ指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e159-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="2e159-117">これらのプロパティが存在しない場合、MAPI はエントリ ポイントが指定されていないと見なします。</span><span class="sxs-lookup"><span data-stu-id="2e159-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="2e159-118">エントリ ポイント関数が表示されるダイナミック リンク ライブラリ (DLL) の名前は、PR_SERVICE_DLL_NAME **(** [PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) プロパティによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="2e159-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="2e159-119">メッセージ サービス エントリ ポイントの詳細については、「Service Provider Entry Point Function の実装 [」を参照してください](implementing-a-service-provider-entry-point-function.md)。</span><span class="sxs-lookup"><span data-stu-id="2e159-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e159-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2e159-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e159-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2e159-121">Header files</span></span>

<span data-ttu-id="2e159-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e159-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e159-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e159-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e159-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e159-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2e159-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2e159-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e159-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e159-126">See also</span></span>



[<span data-ttu-id="2e159-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2e159-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e159-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e159-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e159-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2e159-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e159-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2e159-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

