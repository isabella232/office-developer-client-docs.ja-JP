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
ms.openlocfilehash: d992c7ac43c736e01184e1f12b3ad366587c9b06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802398"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="41c89-103">PidTagAccessControlListTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="41c89-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="41c89-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41c89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41c89-105">すべてのシステム アクセス制御リスト (SACL) のフォルダーに適用されるので構成されるテーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="41c89-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41c89-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="41c89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41c89-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="41c89-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="41c89-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="41c89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41c89-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="41c89-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="41c89-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="41c89-110">Data type:</span></span>  <br/> |<span data-ttu-id="41c89-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="41c89-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="41c89-112">領域:</span><span class="sxs-lookup"><span data-stu-id="41c89-112">Area:</span></span>  <br/> |<span data-ttu-id="41c89-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="41c89-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41c89-114">注釈</span><span class="sxs-lookup"><span data-stu-id="41c89-114">Remarks</span></span>

<span data-ttu-id="41c89-115">このプロパティでは、Exchange Server 上のすべてのフォルダー オブジェクト上に存在します。</span><span class="sxs-lookup"><span data-stu-id="41c89-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="41c89-116">値がこのプロパティに含まれているは、読み取り用に使用され、フォルダーのリスト (Acl) のアクセス制御を変更します。</span><span class="sxs-lookup"><span data-stu-id="41c89-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="41c89-117">**IID_IExchangeModifyTable**インターフェイス識別子を使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用するにを取得するのには、 [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)フォルダーの ACL テーブルへのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="41c89-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="41c89-118">読み取りおよびそれらの Acl を変更するには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="41c89-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="41c89-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="41c89-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="41c89-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="41c89-120">Header files</span></span>

<span data-ttu-id="41c89-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41c89-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="41c89-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="41c89-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="41c89-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41c89-123">Mapitags.h</span></span>
  
> <span data-ttu-id="41c89-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="41c89-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41c89-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="41c89-125">See also</span></span>



[<span data-ttu-id="41c89-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="41c89-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41c89-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="41c89-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41c89-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="41c89-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41c89-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="41c89-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

