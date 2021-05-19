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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433039"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="c630d-103">PidTagMemberEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c630d-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c630d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c630d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c630d-105">システム アクセス制御リスト (SACL) テーブル メンバーのディレクトリ オブジェクトエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="c630d-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c630d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c630d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c630d-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c630d-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c630d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c630d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c630d-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="c630d-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="c630d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c630d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c630d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c630d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c630d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c630d-112">Area:</span></span>  <br/> |<span data-ttu-id="c630d-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="c630d-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c630d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c630d-114">Remarks</span></span>

<span data-ttu-id="c630d-115">このプロパティは [、IExchangeModifyTable](iexchangemodifytableiunknown.md) インターフェイスで使用して、SACL が適用されるユーザーまたは役割を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="c630d-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="c630d-116">SACL テーブルでメンバーを作成した後 **、ENTRYID を** 変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="c630d-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="c630d-117">変更するには、テーブル メンバーを削除し、別の ENTRYID を使用してテーブル メンバーを **再作成する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="c630d-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c630d-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c630d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c630d-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c630d-119">Header files</span></span>

<span data-ttu-id="c630d-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c630d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c630d-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c630d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c630d-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c630d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c630d-123">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c630d-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c630d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c630d-124">See also</span></span>



[<span data-ttu-id="c630d-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c630d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c630d-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c630d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c630d-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c630d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c630d-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c630d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

