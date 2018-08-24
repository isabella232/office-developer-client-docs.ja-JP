---
title: attConversationID and attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582715"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="fb9a7-103">attConversationID and attParentID</span><span class="sxs-lookup"><span data-stu-id="fb9a7-103">attConversationID and attParentID</span></span>

<span data-ttu-id="fb9a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb9a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb9a7-105">ワークグループ 3.1 メールの会話のキーのウィンドウは、テキスト文字列です。</span><span class="sxs-lookup"><span data-stu-id="fb9a7-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="fb9a7-106">MAPI 対応は、バイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="fb9a7-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="fb9a7-107">下位互換性を提供するには、TNEF の実装はバイナリ データをテキストに変換し、終端の null 文字を追加します。</span><span class="sxs-lookup"><span data-stu-id="fb9a7-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fb9a7-108">MAPI に対応するプロパティに、これらの TNEF の属性がマップされている PR_CONVERSATION_KEY と PR_PARENT_KEY では削除されて Microsoft Exchange Server: **PR_CONVERSATION_KEY**PidTagConversationKey の標準的な[の使用プロパティ](pidtagconversationkey-canonical-property.md)、のみは IPM の**を検索するため、Outlook 内で永続化します。MessageManager**メッセージです。</span><span class="sxs-lookup"><span data-stu-id="fb9a7-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fb9a7-109">注釈</span><span class="sxs-lookup"><span data-stu-id="fb9a7-109">Remarks</span></span>

<span data-ttu-id="fb9a7-110">**PR_CONVERSATION_KEY**プロパティは、 **PR_CONVERSATION_INDEX** [PidTagConversationIndex の標準的なプロパティ](pidtagconversationindex-canonical-property.md)と**PR_CONVERSATION_TOPIC**PidTagConversationTopic の標準的な[のそれ以外の場合古い前身プロパティ](pidtagconversationtopic-canonical-property.md)を代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb9a7-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb9a7-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb9a7-111">See also</span></span>

- [<span data-ttu-id="fb9a7-112">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="fb9a7-112">IPM Subtree</span></span>](ipm-subtree.md)
- <span data-ttu-id="fb9a7-113">[MAPI ���ʂȃt�H���_�[](mapi-special-folders.md)</span><span class="sxs-lookup"><span data-stu-id="fb9a7-113">[MAPI Special Folders](mapi-special-folders.md)</span></span>

