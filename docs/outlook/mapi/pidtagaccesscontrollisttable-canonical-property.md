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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332005"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="a23ef-103">PidTagAccessControlListTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a23ef-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="a23ef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a23ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a23ef-105">フォルダーに適用されているすべてのシステムアクセス制御リスト (SACL) で構成されるテーブルが保存されています。</span><span class="sxs-lookup"><span data-stu-id="a23ef-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a23ef-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a23ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a23ef-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="a23ef-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="a23ef-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a23ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a23ef-109">0x3fe0</span><span class="sxs-lookup"><span data-stu-id="a23ef-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="a23ef-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a23ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="a23ef-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a23ef-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a23ef-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a23ef-112">Area:</span></span>  <br/> |<span data-ttu-id="a23ef-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="a23ef-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a23ef-114">解説</span><span class="sxs-lookup"><span data-stu-id="a23ef-114">Remarks</span></span>

<span data-ttu-id="a23ef-115">このプロパティは、Exchange サーバー上のすべての folder オブジェクトに存在します。</span><span class="sxs-lookup"><span data-stu-id="a23ef-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="a23ef-116">このプロパティに含まれる値は、フォルダーのアクセス制御リスト (acl) を読み取って変更するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a23ef-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="a23ef-117">**IID_IExchangeModifyTable**インターフェイス識別子を使用して[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを使用すると、フォルダーの ACL テーブルに対して[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)インターフェイスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="a23ef-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="a23ef-118">このインターフェイスを使用して、これらの acl を読み取りおよび変更できます。</span><span class="sxs-lookup"><span data-stu-id="a23ef-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a23ef-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a23ef-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a23ef-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a23ef-120">Header files</span></span>

<span data-ttu-id="a23ef-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a23ef-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a23ef-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a23ef-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a23ef-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a23ef-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a23ef-124">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a23ef-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a23ef-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a23ef-125">See also</span></span>



[<span data-ttu-id="a23ef-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a23ef-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a23ef-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a23ef-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a23ef-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a23ef-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a23ef-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a23ef-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

