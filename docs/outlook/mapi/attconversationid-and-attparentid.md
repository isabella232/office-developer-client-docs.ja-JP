---
title: attConversationID and attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: f52383c5208fc2288018dcdeb644722e73dfc86a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605182"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID and attParentID

**適用対象**: Outlook 2013 | Outlook 2016 
  
ワークWindows 3.1 メール会話キーのプロパティは、テキスト文字列です。 MAPI に相当する値はバイナリ値です。 下位互換性を提供するために、TNEF 実装はバイナリ データをテキストに変換し、終端の null 文字を追加します。
  
> [!NOTE]
> これらの TNEF 属性がマップされている MAPI の対応するプロパティ PR_CONVERSATION_KEY および PR_PARENT_KEY は、ipM を検索するために Microsoft Exchange Server: **PR_CONVERSATION_KEY** の使用 [、PidTagConversationKey](pidtagconversationkey-canonical-property.md)標準プロパティの使用で使用されなくなったが、Outlook でのみ保持されます。 **MessageManager** メッセージ。 
  
## <a name="remarks"></a>注釈

**PR_CONVERSATION_KEY** プロパティは **、代** わりに使用する必要がある PR_CONVERSATION_INDEX [、PidTagConversationIndex](pidtagconversationindex-canonical-property.md)標準プロパティ、**および PR_CONVERSATION_TOPIC** [、PidTagConversationTopic 標準](pidtagconversationtopic-canonical-property.md)プロパティのそれ以外の場合は古い前駆です。
  
## <a name="see-also"></a>関連項目

- [IPM サブツリー](ipm-subtree.md)
- [MAPI の特別なフォルダー](mapi-special-folders.md)

