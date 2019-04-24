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
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330066"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="3236b-103">PidTagServiceDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3236b-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="3236b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3236b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3236b-105">構成のために呼び出すメッセージサービスプロバイダーエントリポイント関数を含む DLL のファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3236b-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3236b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3236b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3236b-107">PR_SERVICE_DLL_NAME、PR_SERVICE_DLL_NAME_A、PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3236b-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3236b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3236b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3236b-109">0x3d0a</span><span class="sxs-lookup"><span data-stu-id="3236b-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="3236b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3236b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3236b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3236b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3236b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3236b-112">Area:</span></span>  <br/> |<span data-ttu-id="3236b-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="3236b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3236b-114">解説</span><span class="sxs-lookup"><span data-stu-id="3236b-114">Remarks</span></span>

<span data-ttu-id="3236b-115">エントリポイント関数名が**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) メソッドに表示される場合、エントリポイントが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="3236b-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="3236b-116">MAPI は DLL ファイルの名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="3236b-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="3236b-117">文字列32をベース DLL 名に追加して、32ビットプラットフォームで実行されているバージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="3236b-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="3236b-118">たとえば、MAPI という名前があるとします。DLL が指定されている場合、MAPI は MAPI32 という名前を作成します。dll は、対応する32ビットバージョンの dll を表します。</span><span class="sxs-lookup"><span data-stu-id="3236b-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="3236b-119">これらのプロパティは、基本名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3236b-119">These properties should specify the base name.</span></span> <span data-ttu-id="3236b-120">MAPI は、文字列32を必要に応じて追加します。</span><span class="sxs-lookup"><span data-stu-id="3236b-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="3236b-121">これらのプロパティの一部として文字列32を含めると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3236b-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3236b-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3236b-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3236b-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3236b-123">Header files</span></span>

<span data-ttu-id="3236b-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3236b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3236b-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3236b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3236b-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="3236b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3236b-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3236b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3236b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3236b-128">See also</span></span>



[<span data-ttu-id="3236b-129">PidTagProviderDllName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3236b-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="3236b-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3236b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3236b-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3236b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3236b-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3236b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3236b-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3236b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

