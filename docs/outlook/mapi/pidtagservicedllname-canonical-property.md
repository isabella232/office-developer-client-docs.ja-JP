---
title: PidTagServiceDllName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2917f2119fde38686397b65956113bc430b2e31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570815"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="a53f3-103">PidTagServiceDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a53f3-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="a53f3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a53f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a53f3-105">構成にするのにはメッセージ サービス プロバイダーのエントリ ポイント関数を含む DLL のファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a53f3-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a53f3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a53f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a53f3-107">PR_SERVICE_DLL_NAME、PR_SERVICE_DLL_NAME_A、PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a53f3-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a53f3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a53f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a53f3-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="a53f3-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="a53f3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a53f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="a53f3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a53f3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a53f3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a53f3-112">Area:</span></span>  <br/> |<span data-ttu-id="a53f3-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="a53f3-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a53f3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a53f3-114">Remarks</span></span>

<span data-ttu-id="a53f3-115">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) メソッドのエントリ ポイント関数名が表示されたら、エントリ ポイントが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="a53f3-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="a53f3-116">MAPI は、DLL ファイルの名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="a53f3-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="a53f3-117">ベース ファイル名には、DLL を一意に識別する最大 6 つの文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a53f3-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="a53f3-118">MAPI では、32 ビット プラットフォーム上で動作するバージョンを識別する基本の DLL の名前に 32 の文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="a53f3-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="a53f3-119">たとえば、MAPI の名前です。DLL を指定すると、MAPI が MAPI32 名を作成します。DLL が、DLL の対応する 32 ビット バージョンを表す。</span><span class="sxs-lookup"><span data-stu-id="a53f3-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="a53f3-120">これらのプロパティは、基本名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a53f3-120">These properties should specify the base name.</span></span> <span data-ttu-id="a53f3-121">MAPI では、必要に応じて文字列の 32 を追加します。</span><span class="sxs-lookup"><span data-stu-id="a53f3-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="a53f3-122">エラーでこれらのプロパティの結果の一部として 32 の文字列を含みます。</span><span class="sxs-lookup"><span data-stu-id="a53f3-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a53f3-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a53f3-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a53f3-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a53f3-124">Header files</span></span>

<span data-ttu-id="a53f3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a53f3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a53f3-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a53f3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a53f3-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a53f3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a53f3-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a53f3-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a53f3-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a53f3-129">See also</span></span>



[<span data-ttu-id="a53f3-130">PidTagProviderDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a53f3-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="a53f3-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a53f3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a53f3-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a53f3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a53f3-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a53f3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a53f3-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a53f3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

