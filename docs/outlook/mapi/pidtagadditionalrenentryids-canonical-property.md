---
title: PidTagAdditionalRenEntryIds の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802422"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a><span data-ttu-id="f224a-103">PidTagAdditionalRenEntryIds の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f224a-103">PidTagAdditionalRenEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="f224a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f224a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f224a-105">エントリ特定の特殊フォルダーの Id にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f224a-105">Contains the entry IDs of certain special folders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f224a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f224a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f224a-107">PR_ADDITIONAL_REN_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="f224a-107">PR_ADDITIONAL_REN_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="f224a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f224a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f224a-109">0x36D8</span><span class="sxs-lookup"><span data-stu-id="f224a-109">0x36D8</span></span>  <br/> |
|<span data-ttu-id="f224a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f224a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f224a-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="f224a-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="f224a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f224a-112">Area:</span></span>  <br/> |<span data-ttu-id="f224a-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f224a-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f224a-114">備考</span><span class="sxs-lookup"><span data-stu-id="f224a-114">Remarks</span></span>

<span data-ttu-id="f224a-115">この複数値を持つプロパティの最初の 5 つのエントリは、ストア内に存在する場合に、次の特別なフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="f224a-115">The first five entries of this multi-valued property apply to following special folders, if they exist in the store:</span></span>
  
<span data-ttu-id="f224a-116">0 - [競合] フォルダー</span><span class="sxs-lookup"><span data-stu-id="f224a-116">0 - conflicts folder</span></span>
  
<span data-ttu-id="f224a-117">1-同期の失敗フォルダー</span><span class="sxs-lookup"><span data-stu-id="f224a-117">1 - sync issues folder</span></span>
  
<span data-ttu-id="f224a-118">2-ローカルの失敗フォルダー</span><span class="sxs-lookup"><span data-stu-id="f224a-118">2 - local failures folder</span></span>
  
<span data-ttu-id="f224a-119">3-サーバーの失敗] フォルダー</span><span class="sxs-lookup"><span data-stu-id="f224a-119">3 - server failures folder</span></span>
  
<span data-ttu-id="f224a-120">4-迷惑メール フォルダー</span><span class="sxs-lookup"><span data-stu-id="f224a-120">4 - junk email folder</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f224a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f224a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f224a-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f224a-122">Protocol specifications</span></span>

<span data-ttu-id="f224a-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f224a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f224a-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f224a-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f224a-125">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f224a-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f224a-126">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f224a-126">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="f224a-127">[[MS OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f224a-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f224a-128">識別し、だまして受信者 (パスワードやその他の個人情報) などの機密情報を盗み、以外の信頼できる発行元に設計された電子メール メッセージをマークします。</span><span class="sxs-lookup"><span data-stu-id="f224a-128">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
<span data-ttu-id="f224a-129">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f224a-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f224a-130">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="f224a-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f224a-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f224a-131">Header files</span></span>

<span data-ttu-id="f224a-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f224a-132">Mapitags.h</span></span>
  
> <span data-ttu-id="f224a-133">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f224a-133">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="f224a-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f224a-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f224a-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f224a-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f224a-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="f224a-136">See also</span></span>



[<span data-ttu-id="f224a-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f224a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f224a-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f224a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f224a-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f224a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


[<span data-ttu-id="f224a-140">ストア API について</span><span class="sxs-lookup"><span data-stu-id="f224a-140">About the Store API</span></span>](http://msdn.microsoft.com/ja-jp/library/aa192884.aspx)

