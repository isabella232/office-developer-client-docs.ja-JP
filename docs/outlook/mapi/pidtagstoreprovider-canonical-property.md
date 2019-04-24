---
title: PidTagStoreProvider 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278709"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="7063a-103">PidTagStoreProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7063a-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="7063a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7063a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7063a-105">メッセージストアの種類を示すプロバイダー定義の[MAPIUID](mapiuid.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7063a-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7063a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7063a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7063a-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="7063a-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="7063a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7063a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7063a-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="7063a-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="7063a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7063a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7063a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7063a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7063a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7063a-112">Area:</span></span>  <br/> |<span data-ttu-id="7063a-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="7063a-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7063a-114">解説</span><span class="sxs-lookup"><span data-stu-id="7063a-114">Remarks</span></span>

<span data-ttu-id="7063a-115">[MAPIUID](mapiuid.md)構造体は、メッセージストアの種類を識別します。</span><span class="sxs-lookup"><span data-stu-id="7063a-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="7063a-116">この値は、メッセージストアオブジェクトのメッセージストアプロバイダーによって計算され、各プロバイダーに対して一意です。</span><span class="sxs-lookup"><span data-stu-id="7063a-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="7063a-117">通常、メッセージストアテーブルを参照して、必要な種類 (パブリックフォルダーなど) のストアを検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7063a-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="7063a-118">このプロパティは、アドレス帳の**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="7063a-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7063a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7063a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7063a-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7063a-120">Header files</span></span>

<span data-ttu-id="7063a-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7063a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7063a-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7063a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7063a-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7063a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7063a-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7063a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7063a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7063a-125">See also</span></span>



[<span data-ttu-id="7063a-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7063a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7063a-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7063a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7063a-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7063a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7063a-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7063a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

