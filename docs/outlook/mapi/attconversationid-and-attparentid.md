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
# <a name="attconversationid-and-attparentid"></a>attConversationID and attParentID

**適用対象**: Outlook 2013 | Outlook 2016 
  
ワークグループ 3.1 メールの会話のキーのウィンドウは、テキスト文字列です。 MAPI 対応は、バイナリ値です。 下位互換性を提供するには、TNEF の実装はバイナリ データをテキストに変換し、終端の null 文字を追加します。
  
> [!NOTE]
> MAPI に対応するプロパティに、これらの TNEF の属性がマップされている PR_CONVERSATION_KEY と PR_PARENT_KEY では削除されて Microsoft Exchange Server: **PR_CONVERSATION_KEY**PidTagConversationKey の標準的な[の使用プロパティ](pidtagconversationkey-canonical-property.md)、のみは IPM の**を検索するため、Outlook 内で永続化します。MessageManager**メッセージです。 
  
## <a name="remarks"></a>注釈

**PR_CONVERSATION_KEY**プロパティは、 **PR_CONVERSATION_INDEX** [PidTagConversationIndex の標準的なプロパティ](pidtagconversationindex-canonical-property.md)と**PR_CONVERSATION_TOPIC**PidTagConversationTopic の標準的な[のそれ以外の場合古い前身プロパティ](pidtagconversationtopic-canonical-property.md)を代わりに使用する必要があります。
  
## <a name="see-also"></a>関連項目

- [IPM サブツリー](ipm-subtree.md)
- [MAPI ���ʂȃt�H���_�[](mapi-special-folders.md)

