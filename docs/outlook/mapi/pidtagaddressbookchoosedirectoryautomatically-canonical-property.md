---
title: PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409665"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="2ce84-103">PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce84-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="2ce84-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ce84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ce84-105">現在Microsoft Outlook 2010、Microsoft Outlook 2013最も適切なグローバル アドレス一覧 (GAL) または連絡先フォルダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2ce84-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ce84-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ce84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ce84-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="2ce84-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="2ce84-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2ce84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ce84-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="2ce84-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="2ce84-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="2ce84-110">Property type:</span></span>  <br/> |<span data-ttu-id="2ce84-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2ce84-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2ce84-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2ce84-112">Area:</span></span>  <br/> |<span data-ttu-id="2ce84-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="2ce84-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ce84-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2ce84-114">Remarks</span></span>

<span data-ttu-id="2ce84-115">このプロパティは、[アドレス帳の **オプション] ダイアログの** [自動的に選択する] 設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="2ce84-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="2ce84-116">このプロパティが IID_CAPONE_PROF プロファイル セクションに存在し **、true** に設定されている場合、アドレス帳ダイアログは [SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドで指定されたコンテナーに既定で設定されなくなりましたが、Outlook 2010 または Outlook 2013 がダイアログが表示されたコンテキストに適したアドレス帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ce84-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="2ce84-117">これにより、サードパーティのアドレス帳プロバイダーのエクスペリエンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2ce84-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ce84-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ce84-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ce84-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2ce84-119">Header files</span></span>

<span data-ttu-id="2ce84-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ce84-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2ce84-121">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2ce84-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="2ce84-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ce84-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ce84-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ce84-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ce84-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ce84-124">See also</span></span>



[<span data-ttu-id="2ce84-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce84-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ce84-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce84-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ce84-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2ce84-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2ce84-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ce84-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ce84-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ce84-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

