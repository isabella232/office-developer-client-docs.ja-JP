---
title: PidTagContactAddressBookMultipleAddressFlag の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802573"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="76bfb-103">PidTagContactAddressBookMultipleAddressFlag の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76bfb-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="76bfb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76bfb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76bfb-105">連絡先アイテムごとに複数の電子メール アドレスをプロバイダーがサポートする場合は TRUE にするフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="76bfb-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76bfb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="76bfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76bfb-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="76bfb-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="76bfb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="76bfb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76bfb-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="76bfb-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="76bfb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="76bfb-110">Data type:</span></span>  <br/> |<span data-ttu-id="76bfb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="76bfb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="76bfb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="76bfb-112">Area:</span></span>  <br/> |<span data-ttu-id="76bfb-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="76bfb-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76bfb-114">備考</span><span class="sxs-lookup"><span data-stu-id="76bfb-114">Remarks</span></span>

<span data-ttu-id="76bfb-115">このプロパティが TRUE の場合、プロバイダーは電子メール アドレスがない連絡先を許可しません。</span><span class="sxs-lookup"><span data-stu-id="76bfb-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="76bfb-116">FALSE の場合、プロバイダーは、通常の電子メール アドレスがあるかどうかすべての連絡先を示します。</span><span class="sxs-lookup"><span data-stu-id="76bfb-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="76bfb-117">プライマリ電子メール アドレスのみが受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="76bfb-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="76bfb-118">これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="76bfb-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76bfb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76bfb-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="76bfb-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="76bfb-120">Header files</span></span>

<span data-ttu-id="76bfb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76bfb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="76bfb-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76bfb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="76bfb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76bfb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="76bfb-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76bfb-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76bfb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="76bfb-125">See also</span></span>



[<span data-ttu-id="76bfb-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76bfb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76bfb-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76bfb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76bfb-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="76bfb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76bfb-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="76bfb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

