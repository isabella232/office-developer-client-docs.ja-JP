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
ms.openlocfilehash: d75f22af3f8c9184da55ec57e08cf4db832ed174
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803211"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="06a96-103">PidTagProviderDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06a96-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="06a96-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06a96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06a96-105">MAPI サービス プロバイダーのダイナミック リンク ライブラリ (DLL) の基本ファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06a96-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06a96-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="06a96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06a96-107">PR_PROVIDER_DLL_NAME、PR_PROVIDER_DLL_NAME_A、PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="06a96-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="06a96-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="06a96-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06a96-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="06a96-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="06a96-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="06a96-110">Data type:</span></span>  <br/> |<span data-ttu-id="06a96-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06a96-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="06a96-112">領域:</span><span class="sxs-lookup"><span data-stu-id="06a96-112">Area:</span></span>  <br/> |<span data-ttu-id="06a96-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="06a96-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06a96-114">注釈</span><span class="sxs-lookup"><span data-stu-id="06a96-114">Remarks</span></span>

<span data-ttu-id="06a96-115">MAPI は、DLL ファイルの名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="06a96-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="06a96-116">ベース ファイル名には、DLL を一意に識別する最大 6 つの文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06a96-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="06a96-117">MAPI では、32 ビット プラットフォーム上で動作するバージョンを識別する基本の DLL の名前に 32 の文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="06a96-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="06a96-118">たとえば、MAPI の名前です。DLL を指定すると、MAPI が MAPI32 名を作成します。DLL が、DLL の対応する 32 ビット バージョンを表す。</span><span class="sxs-lookup"><span data-stu-id="06a96-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="06a96-119">これらのプロパティは、基本名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06a96-119">These properties should specify the base name.</span></span> <span data-ttu-id="06a96-120">MAPI では、必要に応じて文字列の 32 を追加します。</span><span class="sxs-lookup"><span data-stu-id="06a96-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="06a96-121">このプロパティによりエラーの一部として 32 の文字列を含みます。</span><span class="sxs-lookup"><span data-stu-id="06a96-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06a96-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06a96-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06a96-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="06a96-123">Header files</span></span>

<span data-ttu-id="06a96-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06a96-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="06a96-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06a96-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="06a96-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06a96-126">Mapitags.h</span></span>
  
> <span data-ttu-id="06a96-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06a96-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06a96-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="06a96-128">See also</span></span>



[<span data-ttu-id="06a96-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06a96-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06a96-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06a96-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06a96-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06a96-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06a96-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06a96-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

