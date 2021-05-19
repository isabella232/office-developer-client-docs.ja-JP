---
title: PidTagAccessControlListTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424505"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="8e0cb-103">PidTagAccessControlListTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e0cb-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="8e0cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e0cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e0cb-105">フォルダーに適用されるすべてのシステム アクセス制御リスト (SACL) で構成されるテーブルを格納します。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e0cb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8e0cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e0cb-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="8e0cb-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="8e0cb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8e0cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e0cb-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="8e0cb-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="8e0cb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8e0cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e0cb-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8e0cb-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8e0cb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8e0cb-112">Area:</span></span>  <br/> |<span data-ttu-id="8e0cb-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="8e0cb-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e0cb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8e0cb-114">Remarks</span></span>

<span data-ttu-id="8e0cb-115">このプロパティは、フォルダー上のすべてのフォルダー オブジェクトExchange Server。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="8e0cb-116">このプロパティに含まれる値は、フォルダーのアクセス制御リスト (ACL) の読み取りおよび変更に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="8e0cb-117">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを **IID_IExchangeModifyTable** インターフェイス識別子と一緒に使用して [、IExchangeModifyTable : フォルダー](iexchangemodifytableiunknown.md)の ACL テーブルへの IUnknown インターフェイスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="8e0cb-118">このインターフェイスを使用して、これらの ACL を読み取り、変更できます。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e0cb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e0cb-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8e0cb-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8e0cb-120">Header files</span></span>

<span data-ttu-id="8e0cb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e0cb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e0cb-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e0cb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e0cb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8e0cb-124">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8e0cb-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e0cb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e0cb-125">See also</span></span>



[<span data-ttu-id="8e0cb-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8e0cb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e0cb-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e0cb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e0cb-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8e0cb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e0cb-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8e0cb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

