---
title: PidTagServiceDeleteFiles 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436826"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="742db-103">PidTagServiceDeleteFiles 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="742db-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="742db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="742db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="742db-105">メッセージサービスがアンインストールされたときに削除されるファイル名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="742db-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="742db-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="742db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="742db-107">PR_SERVICE_DELETE_FILES、PR_SERVICE_DELETE_FILES_A、PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="742db-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="742db-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="742db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="742db-109">0x3d10</span><span class="sxs-lookup"><span data-stu-id="742db-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="742db-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="742db-110">Data type:</span></span>  <br/> |<span data-ttu-id="742db-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="742db-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="742db-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="742db-112">Area:</span></span>  <br/> |<span data-ttu-id="742db-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="742db-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="742db-114">注釈</span><span class="sxs-lookup"><span data-stu-id="742db-114">Remarks</span></span>

<span data-ttu-id="742db-115">これらのプロパティに含まれるリスト内のファイル名は、コントロールパネルを使用してメッセージサービスをアンインストールするときにコンピューターから削除されます。</span><span class="sxs-lookup"><span data-stu-id="742db-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="742db-116">複数のメッセージサービスをサポートする DLL がリストに含まれていない場合、または追加のメッセージサービスが誤って削除された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="742db-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="742db-117">MAPI は、ファイル名、およびその他の文字列が ANSI 文字セットに渡された場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="742db-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="742db-118">OEM 文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="742db-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="742db-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="742db-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="742db-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="742db-120">Header files</span></span>

<span data-ttu-id="742db-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="742db-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="742db-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="742db-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="742db-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="742db-123">Mapitags.h</span></span>
  
> <span data-ttu-id="742db-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="742db-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="742db-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="742db-125">See also</span></span>



[<span data-ttu-id="742db-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="742db-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="742db-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="742db-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="742db-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="742db-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="742db-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="742db-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

