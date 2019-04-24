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
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342638"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="1405e-103">PidTagMemberId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1405e-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="1405e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1405e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1405e-105">Microsoft Exchange Server フォルダーまたはメールボックスについて、説明されている権限を持つテーブルメンバの識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="1405e-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1405e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1405e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1405e-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="1405e-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="1405e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1405e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1405e-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="1405e-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="1405e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1405e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1405e-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="1405e-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="1405e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1405e-112">Area:</span></span>  <br/> |<span data-ttu-id="1405e-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="1405e-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1405e-114">解説</span><span class="sxs-lookup"><span data-stu-id="1405e-114">Remarks</span></span>

<span data-ttu-id="1405e-115">このプロパティは、テーブルに固有の識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="1405e-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="1405e-116">ディレクトリのユーザー識別子は各メンバー識別子に関連付けられ、このプロパティによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="1405e-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="1405e-117">このプロパティは、フォルダーの明示的な権限を持つメンバーのディレクトリエントリ識別子を取得するために[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="1405e-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1405e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1405e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1405e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1405e-119">Protocol specifications</span></span>

<span data-ttu-id="1405e-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1405e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1405e-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1405e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1405e-122">[[OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1405e-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1405e-123">サーバーに格納されているフォルダーのアクセス許可リストの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="1405e-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1405e-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1405e-124">Header files</span></span>

<span data-ttu-id="1405e-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1405e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1405e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1405e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1405e-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1405e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1405e-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1405e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1405e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1405e-129">See also</span></span>



[<span data-ttu-id="1405e-130">PidTagMemberEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1405e-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="1405e-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1405e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1405e-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1405e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1405e-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1405e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1405e-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1405e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

