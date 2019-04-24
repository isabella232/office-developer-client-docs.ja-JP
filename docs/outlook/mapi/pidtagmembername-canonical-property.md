---
title: PidTagMemberName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342484"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="cef56-103">PidTagMemberName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cef56-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="cef56-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cef56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cef56-105">アクセス制御リスト (ACL) テーブルのメンバの表示名を含みます。</span><span class="sxs-lookup"><span data-stu-id="cef56-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cef56-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cef56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cef56-107">PR_MEMBER_NAME、PR_MEMBER_NAME_A、PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="cef56-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="cef56-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cef56-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cef56-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="cef56-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="cef56-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cef56-110">Data type:</span></span>  <br/> |<span data-ttu-id="cef56-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cef56-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cef56-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cef56-112">Area:</span></span>  <br/> |<span data-ttu-id="cef56-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="cef56-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cef56-114">解説</span><span class="sxs-lookup"><span data-stu-id="cef56-114">Remarks</span></span>

<span data-ttu-id="cef56-115">[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)インターフェイスでは、これらのプロパティを使用して、フォルダーまたはメールボックスに対する明示的な権限を持つ個人または役割である ACL テーブルのメンバーの名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="cef56-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cef56-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cef56-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cef56-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cef56-117">Protocol specifications</span></span>

<span data-ttu-id="cef56-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cef56-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cef56-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cef56-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cef56-120">[[OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cef56-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cef56-121">サーバーに格納されているフォルダーのアクセス許可リストの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="cef56-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cef56-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="cef56-122">Header files</span></span>

<span data-ttu-id="cef56-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cef56-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="cef56-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cef56-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="cef56-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="cef56-125">Mapitags.h</span></span>
  
> <span data-ttu-id="cef56-126">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cef56-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cef56-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="cef56-127">See also</span></span>



[<span data-ttu-id="cef56-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cef56-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="cef56-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cef56-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cef56-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cef56-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cef56-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cef56-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cef56-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cef56-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

