---
title: PidTagAdditionalRenEntryIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282362"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a><span data-ttu-id="7a69c-103">PidTagAdditionalRenEntryIds 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a69c-103">PidTagAdditionalRenEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="7a69c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a69c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a69c-105">特定の特別なフォルダーのエントリの ID を格納します。</span><span class="sxs-lookup"><span data-stu-id="7a69c-105">Contains the entry IDs of certain special folders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a69c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7a69c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a69c-107">PR_ADDITIONAL_REN_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="7a69c-107">PR_ADDITIONAL_REN_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="7a69c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7a69c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a69c-109">0x36D8</span><span class="sxs-lookup"><span data-stu-id="7a69c-109">0x36D8</span></span>  <br/> |
|<span data-ttu-id="7a69c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7a69c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a69c-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="7a69c-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="7a69c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7a69c-112">Area:</span></span>  <br/> |<span data-ttu-id="7a69c-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="7a69c-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a69c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7a69c-114">Remarks</span></span>

<span data-ttu-id="7a69c-115">この複数値プロパティの最初の 5 つのエントリは、ストアに存在する場合、次の特別なフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="7a69c-115">The first five entries of this multi-valued property apply to following special folders, if they exist in the store:</span></span>
  
<span data-ttu-id="7a69c-116">0 - 競合フォルダー</span><span class="sxs-lookup"><span data-stu-id="7a69c-116">0 - conflicts folder</span></span>
  
<span data-ttu-id="7a69c-117">1 - 同期の問題フォルダー</span><span class="sxs-lookup"><span data-stu-id="7a69c-117">1 - sync issues folder</span></span>
  
<span data-ttu-id="7a69c-118">2 - ローカルエラー フォルダー</span><span class="sxs-lookup"><span data-stu-id="7a69c-118">2 - local failures folder</span></span>
  
<span data-ttu-id="7a69c-119">3 - サーバー障害フォルダー</span><span class="sxs-lookup"><span data-stu-id="7a69c-119">3 - server failures folder</span></span>
  
<span data-ttu-id="7a69c-120">4 - 迷惑メール フォルダー</span><span class="sxs-lookup"><span data-stu-id="7a69c-120">4 - junk email folder</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a69c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a69c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a69c-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7a69c-122">Protocol specifications</span></span>

<span data-ttu-id="7a69c-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a69c-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a69c-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="7a69c-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a69c-125">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a69c-125">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a69c-126">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a69c-126">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="7a69c-127">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a69c-127">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a69c-128">受信者を騙して機密情報 (パスワードや他の個人情報など) を信頼できないソースに開示するように設計された電子メール メッセージを識別およびマークします。</span><span class="sxs-lookup"><span data-stu-id="7a69c-128">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
<span data-ttu-id="7a69c-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a69c-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a69c-130">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="7a69c-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a69c-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a69c-131">Header files</span></span>

<span data-ttu-id="7a69c-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a69c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="7a69c-133">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="7a69c-133">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="7a69c-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a69c-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a69c-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a69c-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a69c-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a69c-136">See also</span></span>



[<span data-ttu-id="7a69c-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a69c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a69c-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7a69c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a69c-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7a69c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


[<span data-ttu-id="7a69c-140">ストア API について</span><span class="sxs-lookup"><span data-stu-id="7a69c-140">About the Store API</span></span>](https://msdn.microsoft.com/library/aa192884.aspx)

