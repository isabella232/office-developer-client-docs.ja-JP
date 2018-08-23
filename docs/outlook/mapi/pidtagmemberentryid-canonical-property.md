---
title: PidTagMemberEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 27659b69e0ae050206de18c1258ee593737fbd3b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592949"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="57db8-103">PidTagMemberEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="57db8-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="57db8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57db8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57db8-105">システム アクセス制御リスト (SACL) テーブルのメンバーのディレクトリ オブジェクトのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="57db8-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57db8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="57db8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57db8-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="57db8-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="57db8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="57db8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57db8-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="57db8-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="57db8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="57db8-110">Data type:</span></span>  <br/> |<span data-ttu-id="57db8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="57db8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="57db8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="57db8-112">Area:</span></span>  <br/> |<span data-ttu-id="57db8-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="57db8-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57db8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="57db8-114">Remarks</span></span>

<span data-ttu-id="57db8-115">[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスはこのプロパティを使用して、人や、SACL が適用されるロールを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="57db8-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="57db8-116">SACL の表に、メンバーが作成されると、**エントリ ID**は変更できません。</span><span class="sxs-lookup"><span data-stu-id="57db8-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="57db8-117">それを変更するには、テーブルのメンバーを削除し、別の**エントリ ID**で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57db8-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="57db8-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="57db8-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="57db8-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="57db8-119">Header files</span></span>

<span data-ttu-id="57db8-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57db8-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="57db8-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="57db8-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="57db8-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57db8-122">Mapitags.h</span></span>
  
> <span data-ttu-id="57db8-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="57db8-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57db8-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="57db8-124">See also</span></span>



[<span data-ttu-id="57db8-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="57db8-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57db8-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="57db8-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57db8-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="57db8-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57db8-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="57db8-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

