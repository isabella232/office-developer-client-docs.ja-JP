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
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342498"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="aaf56-103">PidTagMemberEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf56-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="aaf56-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf56-105">システムアクセス制御リスト (SACL) テーブルメンバーのディレクトリオブジェクトエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="aaf56-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aaf56-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="aaf56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aaf56-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aaf56-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="aaf56-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aaf56-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aaf56-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="aaf56-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="aaf56-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="aaf56-110">Data type:</span></span>  <br/> |<span data-ttu-id="aaf56-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aaf56-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aaf56-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="aaf56-112">Area:</span></span>  <br/> |<span data-ttu-id="aaf56-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="aaf56-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaf56-114">解説</span><span class="sxs-lookup"><span data-stu-id="aaf56-114">Remarks</span></span>

<span data-ttu-id="aaf56-115">このプロパティは、 [IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスで、SACL が適用される個人または役割を一意に識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aaf56-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="aaf56-116">SACL テーブルにメンバーを作成した後は、 **ENTRYID**を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="aaf56-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="aaf56-117">変更するには、table メンバーを削除して、別の**ENTRYID**で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf56-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aaf56-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aaf56-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aaf56-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="aaf56-119">Header files</span></span>

<span data-ttu-id="aaf56-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aaf56-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="aaf56-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aaf56-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="aaf56-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="aaf56-122">Mapitags.h</span></span>
  
> <span data-ttu-id="aaf56-123">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aaf56-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aaf56-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="aaf56-124">See also</span></span>



[<span data-ttu-id="aaf56-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf56-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aaf56-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf56-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aaf56-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aaf56-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aaf56-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aaf56-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

