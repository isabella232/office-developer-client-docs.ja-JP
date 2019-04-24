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
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351073"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="b4a43-103">PidTagServiceEntryName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4a43-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="b4a43-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4a43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4a43-105">メッセージサービスを構成するためのエントリポイント関数の名前を含みます。</span><span class="sxs-lookup"><span data-stu-id="b4a43-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4a43-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b4a43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4a43-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="b4a43-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="b4a43-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b4a43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4a43-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="b4a43-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="b4a43-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b4a43-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4a43-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b4a43-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b4a43-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b4a43-112">Area:</span></span>  <br/> |<span data-ttu-id="b4a43-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="b4a43-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4a43-114">解説</span><span class="sxs-lookup"><span data-stu-id="b4a43-114">Remarks</span></span>

<span data-ttu-id="b4a43-115">メッセージサービスの実装者は、メッセージサービスのエントリポイントを指定することをお勧めしますが、エントリポイントは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="b4a43-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="b4a43-116">ただし、関連する構成プロパティが存在する場合にのみ、エントリポイントを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4a43-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="b4a43-117">これらのプロパティが存在しない場合、MAPI はエントリポイントが提供されていないことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="b4a43-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="b4a43-118">エントリポイント関数が表示されるダイナミックリンクライブラリ (DLL) は、 **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) プロパティによって名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="b4a43-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b4a43-119">メッセージサービスのエントリポイントの詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4a43-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4a43-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b4a43-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b4a43-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b4a43-121">Header files</span></span>

<span data-ttu-id="b4a43-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4a43-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4a43-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4a43-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4a43-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b4a43-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b4a43-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4a43-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4a43-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4a43-126">See also</span></span>



[<span data-ttu-id="b4a43-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b4a43-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4a43-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4a43-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4a43-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b4a43-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4a43-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b4a43-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

