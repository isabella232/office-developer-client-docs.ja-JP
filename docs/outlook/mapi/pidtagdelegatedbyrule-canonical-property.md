---
title: PidTagDelegatedByRule 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegatedByRule
api_type:
- HeaderDef
ms.assetid: 284b5001-5de6-4c4e-8e5c-0593ae1b301f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 47458e2468215c6539ad07533c36564d37da8b96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359921"
---
# <a name="pidtagdelegatedbyrule-canonical-property"></a><span data-ttu-id="49cb6-103">PidTagDelegatedByRule 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49cb6-103">PidTagDelegatedByRule Canonical Property</span></span>

  
  
<span data-ttu-id="49cb6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49cb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49cb6-105">フォルダーのメッセージがルールによって委任されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="49cb6-105">Indicates whether a folder's message is delegated by a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49cb6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="49cb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49cb6-107">PR_DELEGATED_BY_RULE</span><span class="sxs-lookup"><span data-stu-id="49cb6-107">PR_DELEGATED_BY_RULE</span></span>  <br/> |
|<span data-ttu-id="49cb6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="49cb6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49cb6-109">0x3fe3</span><span class="sxs-lookup"><span data-stu-id="49cb6-109">0x3FE3</span></span>  <br/> |
|<span data-ttu-id="49cb6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="49cb6-110">Data type:</span></span>  <br/> |<span data-ttu-id="49cb6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="49cb6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="49cb6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="49cb6-112">Area:</span></span>  <br/> |<span data-ttu-id="49cb6-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="49cb6-113">MAPI status</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="49cb6-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="49cb6-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49cb6-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="49cb6-115">Protocol specifications</span></span>

<span data-ttu-id="49cb6-116">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49cb6-116">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49cb6-117">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="49cb6-117">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="49cb6-118">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49cb6-118">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49cb6-119">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="49cb6-119">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49cb6-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="49cb6-120">Header files</span></span>

<span data-ttu-id="49cb6-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49cb6-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="49cb6-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="49cb6-122">Provides data type definitions</span></span>
    
<span data-ttu-id="49cb6-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="49cb6-123">Mapitags.h</span></span>
  
> <span data-ttu-id="49cb6-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="49cb6-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49cb6-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="49cb6-125">See also</span></span>



[<span data-ttu-id="49cb6-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="49cb6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49cb6-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49cb6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49cb6-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="49cb6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49cb6-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="49cb6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

