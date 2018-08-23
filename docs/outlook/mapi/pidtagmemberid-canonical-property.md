---
title: PidTagMemberId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802985"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="519db-103">PidTagMemberId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="519db-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="519db-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="519db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="519db-105">権限を持つ、説明されている Microsoft Exchange Server のフォルダーまたはメールボックスのテーブルのメンバーの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="519db-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="519db-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="519db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="519db-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="519db-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="519db-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="519db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="519db-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="519db-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="519db-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="519db-110">Data type:</span></span>  <br/> |<span data-ttu-id="519db-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="519db-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="519db-112">領域:</span><span class="sxs-lookup"><span data-stu-id="519db-112">Area:</span></span>  <br/> |<span data-ttu-id="519db-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="519db-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="519db-114">注釈</span><span class="sxs-lookup"><span data-stu-id="519db-114">Remarks</span></span>

<span data-ttu-id="519db-115">このプロパティでは、テーブルに一意な識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="519db-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="519db-116">ディレクトリのユーザー id は、各メンバーの識別子に関連付けられたし、はこのプロパティで指定します。</span><span class="sxs-lookup"><span data-stu-id="519db-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="519db-117">このプロパティは、フォルダーに対する明示的な権限を持つメンバーのディレクトリ エントリの識別子を取得するために[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスが使用します。</span><span class="sxs-lookup"><span data-stu-id="519db-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="519db-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="519db-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="519db-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="519db-119">Protocol specifications</span></span>

<span data-ttu-id="519db-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="519db-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="519db-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="519db-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="519db-122">[[MS OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="519db-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="519db-123">サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="519db-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="519db-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="519db-124">Header files</span></span>

<span data-ttu-id="519db-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="519db-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="519db-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="519db-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="519db-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="519db-127">Mapitags.h</span></span>
  
> <span data-ttu-id="519db-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="519db-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="519db-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="519db-129">See also</span></span>



[<span data-ttu-id="519db-130">PidTagMemberEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="519db-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="519db-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="519db-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="519db-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="519db-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="519db-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="519db-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="519db-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="519db-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

