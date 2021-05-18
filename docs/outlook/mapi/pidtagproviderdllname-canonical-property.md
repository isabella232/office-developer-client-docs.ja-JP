---
title: PidTagProviderDllName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286489"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="dc499-103">PidTagProviderDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc499-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="dc499-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc499-105">MAPI サービス プロバイダーのダイナミック リンク ライブラリ (DLL) の基本ファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dc499-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc499-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dc499-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc499-107">PR_PROVIDER_DLL_NAME、PR_PROVIDER_DLL_NAME_A、PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="dc499-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="dc499-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dc499-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc499-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="dc499-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="dc499-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dc499-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc499-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dc499-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dc499-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="dc499-112">Area:</span></span>  <br/> |<span data-ttu-id="dc499-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="dc499-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc499-114">注釈</span><span class="sxs-lookup"><span data-stu-id="dc499-114">Remarks</span></span>

<span data-ttu-id="dc499-115">MAPI では、DLL ファイルの名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc499-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="dc499-116">文字列 32 を基本 DLL 名に追加して、32 ビット プラットフォームで実行されるバージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="dc499-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="dc499-117">たとえば、名前を指定MAPI.DLL MAPI は、対応する 32 ビット バージョンの DLL を表す名前 MAPI32.DLL を作成します。</span><span class="sxs-lookup"><span data-stu-id="dc499-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="dc499-118">これらのプロパティには、基本名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc499-118">These properties should specify the base name.</span></span> <span data-ttu-id="dc499-119">MAPI は、必要に応じて文字列 32 を追加します。</span><span class="sxs-lookup"><span data-stu-id="dc499-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="dc499-120">このプロパティの一部として文字列 32 を含めた場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="dc499-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc499-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dc499-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dc499-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dc499-122">Header files</span></span>

<span data-ttu-id="dc499-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc499-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc499-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc499-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc499-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc499-125">Mapitags.h</span></span>
  
> <span data-ttu-id="dc499-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="dc499-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc499-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc499-127">See also</span></span>



[<span data-ttu-id="dc499-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="dc499-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc499-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc499-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc499-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="dc499-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc499-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="dc499-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

