---
title: PidTagAddressBookChooseDirectoryAutomatically の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802433"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="a75a6-103">PidTagAddressBookChooseDirectoryAutomatically の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a75a6-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="a75a6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a75a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a75a6-105">最も適切なグローバル アドレス一覧 (GAL) を選択するか、現在のメールボックスの連絡先フォルダーには、Microsoft Outlook 2010 と Microsoft Outlook 2013 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a75a6-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a75a6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a75a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a75a6-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="a75a6-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="a75a6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a75a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a75a6-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="a75a6-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="a75a6-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="a75a6-110">Property type:</span></span>  <br/> |<span data-ttu-id="a75a6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a75a6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a75a6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a75a6-112">Area:</span></span>  <br/> |<span data-ttu-id="a75a6-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="a75a6-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a75a6-114">備考</span><span class="sxs-lookup"><span data-stu-id="a75a6-114">Remarks</span></span>

<span data-ttu-id="a75a6-115">このプロパティは、アドレス帳のオプション] ダイアログ ボックスで**自動的に選択**の設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="a75a6-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="a75a6-116">このプロパティが IID_CAPONE_PROF のプロファイル セクション内に存在する、Outlook 2010 または Outlook 2013 に**true を指定**アドレス帳ダイアログ不要になった、 [SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドで指定されたコンテナーのデフォルトが、アドレス帳を選択する設定は、ダイアログ ボックスが表示されていたコンテキストに適したと見なされます。</span><span class="sxs-lookup"><span data-stu-id="a75a6-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="a75a6-117">ありますが低い経験ではサード パーティのアドレス帳プロバイダーに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a75a6-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a75a6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a75a6-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a75a6-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a75a6-119">Header files</span></span>

<span data-ttu-id="a75a6-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a75a6-120">Mapitags.h</span></span>
  
> <span data-ttu-id="a75a6-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a75a6-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="a75a6-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a75a6-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a75a6-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a75a6-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a75a6-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a75a6-124">See also</span></span>



[<span data-ttu-id="a75a6-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a75a6-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a75a6-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a75a6-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a75a6-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a75a6-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a75a6-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a75a6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a75a6-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a75a6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

