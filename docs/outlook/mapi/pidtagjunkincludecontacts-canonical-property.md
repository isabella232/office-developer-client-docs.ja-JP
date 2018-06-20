---
title: PidTagJunkIncludeContacts の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802914"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="15a32-103">PidTagJunkIncludeContacts の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="15a32-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="15a32-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15a32-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15a32-105">連絡先フォルダー内の連絡先の電子メール アドレスが迷惑メール フィルターについては特別に扱うかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="15a32-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15a32-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="15a32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15a32-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="15a32-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="15a32-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="15a32-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15a32-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="15a32-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="15a32-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="15a32-110">Data type:</span></span>  <br/> |<span data-ttu-id="15a32-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15a32-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15a32-112">領域:</span><span class="sxs-lookup"><span data-stu-id="15a32-112">Area:</span></span>  <br/> |<span data-ttu-id="15a32-113">スパム</span><span class="sxs-lookup"><span data-stu-id="15a32-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15a32-114">備考</span><span class="sxs-lookup"><span data-stu-id="15a32-114">Remarks</span></span>

<span data-ttu-id="15a32-115">"0x00000001"に設定すると、これらの電子メール アドレスする必要がありますを先に設定、迷惑メール ルールの制限の「信頼された」の連絡先電子メール アドレスの部分をこれらのアドレスからのメールが「迷惑メール」として扱われます。</span><span class="sxs-lookup"><span data-stu-id="15a32-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="15a32-116">"0x00000000"に設定すると、連絡先フォルダーから電子メール アドレスする必要がありますに追加できません迷惑メールのルールとルールのセクションは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="15a32-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="15a32-117">このプロパティが"0x00000001"と追加した連絡先が迷惑メール ルールの「信頼されたアドレス帳にまだ含まれていない電子メール アドレスを持つ場合の値である場合制限これらの電子メール アドレスを追加しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="15a32-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="15a32-118">このプロパティが"0x00000000"の場合は、操作する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="15a32-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15a32-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="15a32-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15a32-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="15a32-120">Protocol specifications</span></span>

<span data-ttu-id="15a32-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a32-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a32-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="15a32-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15a32-123">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15a32-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15a32-124">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="15a32-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15a32-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="15a32-125">Header files</span></span>

<span data-ttu-id="15a32-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15a32-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="15a32-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="15a32-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="15a32-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15a32-128">Mapitags.h</span></span>
  
> <span data-ttu-id="15a32-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15a32-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15a32-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="15a32-130">See also</span></span>



[<span data-ttu-id="15a32-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="15a32-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15a32-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="15a32-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15a32-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="15a32-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15a32-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="15a32-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

