---
title: PidTagMemberEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802977"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="a4786-103">PidTagMemberEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a4786-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a4786-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4786-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4786-105">システム アクセス制御リスト (SACL) テーブルのメンバーのディレクトリ オブジェクトのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a4786-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4786-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a4786-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4786-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a4786-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a4786-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a4786-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4786-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="a4786-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="a4786-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a4786-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4786-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a4786-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a4786-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a4786-112">Area:</span></span>  <br/> |<span data-ttu-id="a4786-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="a4786-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4786-114">備考</span><span class="sxs-lookup"><span data-stu-id="a4786-114">Remarks</span></span>

<span data-ttu-id="a4786-115">[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスはこのプロパティを使用して、人や、SACL が適用されるロールを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="a4786-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="a4786-116">SACL の表に、メンバーが作成されると、**エントリ ID**は変更できません。</span><span class="sxs-lookup"><span data-stu-id="a4786-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="a4786-117">それを変更するには、テーブルのメンバーを削除し、別の**エントリ ID**で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4786-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4786-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a4786-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4786-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a4786-119">Header files</span></span>

<span data-ttu-id="a4786-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4786-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4786-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a4786-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4786-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4786-122">Mapitags.h</span></span>
  
> <span data-ttu-id="a4786-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a4786-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4786-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4786-124">See also</span></span>



[<span data-ttu-id="a4786-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4786-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4786-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4786-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4786-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a4786-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4786-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a4786-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

