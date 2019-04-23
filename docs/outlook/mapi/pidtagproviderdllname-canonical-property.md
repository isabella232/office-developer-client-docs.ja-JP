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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980460"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="babb2-103">PidTagProviderDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="babb2-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="babb2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="babb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="babb2-105">MAPI サービスプロバイダーのダイナミックリンクライブラリ (DLL) のベースファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="babb2-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="babb2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="babb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="babb2-107">PR_PROVIDER_DLL_NAME、PR_PROVIDER_DLL_NAME_A、PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="babb2-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="babb2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="babb2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="babb2-109">0x300a</span><span class="sxs-lookup"><span data-stu-id="babb2-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="babb2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="babb2-110">Data type:</span></span>  <br/> |<span data-ttu-id="babb2-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="babb2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="babb2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="babb2-112">Area:</span></span>  <br/> |<span data-ttu-id="babb2-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="babb2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="babb2-114">解説</span><span class="sxs-lookup"><span data-stu-id="babb2-114">Remarks</span></span>

<span data-ttu-id="babb2-115">MAPI は DLL ファイルの名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="babb2-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="babb2-116">文字列32をベース DLL 名に追加して、32ビットプラットフォームで実行されているバージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="babb2-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="babb2-117">たとえば、MAPI という名前があるとします。DLL が指定されている場合、MAPI は MAPI32 という名前を作成します。dll は、対応する32ビットバージョンの dll を表します。</span><span class="sxs-lookup"><span data-stu-id="babb2-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="babb2-118">これらのプロパティは、基本名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="babb2-118">These properties should specify the base name.</span></span> <span data-ttu-id="babb2-119">MAPI は、文字列32を必要に応じて追加します。</span><span class="sxs-lookup"><span data-stu-id="babb2-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="babb2-120">このプロパティの一部として文字列32を含めると、エラーになります。</span><span class="sxs-lookup"><span data-stu-id="babb2-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="babb2-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="babb2-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="babb2-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="babb2-122">Header files</span></span>

<span data-ttu-id="babb2-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="babb2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="babb2-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="babb2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="babb2-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="babb2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="babb2-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="babb2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="babb2-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="babb2-127">See also</span></span>



[<span data-ttu-id="babb2-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="babb2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="babb2-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="babb2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="babb2-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="babb2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="babb2-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="babb2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

