---
title: PidTagContactAddressBookMultipleAddressFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802562"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="8f511-103">PidTagContactAddressBookMultipleAddressFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8f511-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="8f511-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f511-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f511-105">連絡先アイテムごとでは、プロバイダーが複数の電子メールをサポートするかどうかを示すフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f511-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f511-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8f511-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f511-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8f511-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="8f511-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8f511-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f511-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="8f511-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="8f511-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8f511-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f511-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="8f511-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="8f511-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8f511-112">Area:</span></span>  <br/> |<span data-ttu-id="8f511-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="8f511-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f511-114">備考</span><span class="sxs-lookup"><span data-stu-id="8f511-114">Remarks</span></span>

<span data-ttu-id="8f511-115">このプロパティのフラグが TRUE の場合は、プロバイダーでは、この電子メール アドレスがない連絡先は含まれません。</span><span class="sxs-lookup"><span data-stu-id="8f511-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="8f511-116">プライマリ電子メール アドレスのみが受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="8f511-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="8f511-117">これは、アドレス帳の連絡先のプロファイル セクションのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="8f511-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f511-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8f511-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8f511-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8f511-119">Header files</span></span>

<span data-ttu-id="8f511-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f511-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f511-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8f511-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f511-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8f511-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8f511-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f511-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f511-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f511-124">See also</span></span>



[<span data-ttu-id="8f511-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f511-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f511-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f511-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f511-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8f511-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f511-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8f511-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

