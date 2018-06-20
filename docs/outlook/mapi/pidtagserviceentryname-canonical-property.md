---
title: PidTagServiceEntryName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803527"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="ba533-103">PidTagServiceEntryName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ba533-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="ba533-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba533-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba533-105">メッセージ サービスの構成のエントリ ポイント関数の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba533-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba533-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ba533-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba533-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="ba533-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="ba533-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ba533-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba533-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="ba533-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="ba533-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ba533-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba533-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ba533-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ba533-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ba533-112">Area:</span></span>  <br/> |<span data-ttu-id="ba533-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba533-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba533-114">備考</span><span class="sxs-lookup"><span data-stu-id="ba533-114">Remarks</span></span>

<span data-ttu-id="ba533-115">メッセージ サービスのエントリ ポイントを提供するメッセージ サービスの実装者が、エントリ ポイントが必要ではないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba533-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="ba533-116">ただし、エントリ ポイントは、関連する設定のプロパティが存在する場合にのみ指定してください。</span><span class="sxs-lookup"><span data-stu-id="ba533-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="ba533-117">MAPI ではこれらのプロパティが存在しない場合、エントリ ポイントが指定されていないと見なされます。</span><span class="sxs-lookup"><span data-stu-id="ba533-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="ba533-118">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) は、エントリ ポイント関数が入力されているダイナミック リンク ライブラリ (DLL) と呼びます。</span><span class="sxs-lookup"><span data-stu-id="ba533-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ba533-119">メッセージ サービスのエントリ ポイントの詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba533-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba533-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ba533-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba533-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ba533-121">Header files</span></span>

<span data-ttu-id="ba533-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba533-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba533-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ba533-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba533-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba533-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ba533-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba533-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba533-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba533-126">See also</span></span>



[<span data-ttu-id="ba533-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba533-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba533-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba533-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba533-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ba533-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba533-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ba533-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

