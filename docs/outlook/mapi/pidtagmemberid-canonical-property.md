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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342638"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="43962-103">PidTagMemberId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43962-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="43962-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43962-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43962-105">特定のフォルダーまたはメールボックスに対する記述された権限を持つテーブル メンバー Microsoft Exchange Server格納します。</span><span class="sxs-lookup"><span data-stu-id="43962-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43962-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="43962-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43962-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="43962-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="43962-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="43962-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43962-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="43962-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="43962-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="43962-110">Data type:</span></span>  <br/> |<span data-ttu-id="43962-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="43962-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="43962-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="43962-112">Area:</span></span>  <br/> |<span data-ttu-id="43962-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="43962-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43962-114">注釈</span><span class="sxs-lookup"><span data-stu-id="43962-114">Remarks</span></span>

<span data-ttu-id="43962-115">このプロパティは、テーブルに固有の識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="43962-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="43962-116">ディレクトリ ユーザー識別子は、各メンバー識別子に関連付け、このプロパティによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="43962-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="43962-117">このプロパティは [、IExchangeModifyTable](iexchangemodifytableiunknown.md) インターフェイスで使用して、フォルダーに対する明示的な権限を持つメンバーのディレクトリ エントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="43962-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43962-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="43962-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43962-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="43962-119">Protocol specifications</span></span>

<span data-ttu-id="43962-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43962-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43962-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="43962-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43962-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43962-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43962-123">サーバーに保存されているフォルダーのアクセス許可リストの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="43962-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43962-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="43962-124">Header files</span></span>

<span data-ttu-id="43962-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43962-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="43962-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="43962-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="43962-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43962-127">Mapitags.h</span></span>
  
> <span data-ttu-id="43962-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="43962-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43962-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="43962-129">See also</span></span>



[<span data-ttu-id="43962-130">PidTagMemberEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43962-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="43962-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="43962-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43962-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43962-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43962-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="43962-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43962-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="43962-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

