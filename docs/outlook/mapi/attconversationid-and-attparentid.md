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
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318418"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID and attParentID

**適用対象**: Outlook 2013 | Outlook 2016 
  
[ワークグループの Windows 用] 3.1 メールの会話キーはテキスト文字列です。 MAPI に相当する値はバイナリ値です。 下位互換性を確保するために、TNEF 実装はバイナリデータをテキストに変換し、終端の null 文字を追加します。
  
> [!NOTE]
> これらの TNEF 属性がマップされている MAPI の対応するプロパティ、PR_CONVERSATION_KEY および PR_PARENT_KEY は、Microsoft Exchange Server で廃止されました。 **PR_CONVERSATION_KEY**の使用、 [PidTagConversationKey 標準プロパティ](pidtagconversationkey-canonical-property.md)は、IPM を検索する場合にのみ、Outlook で保持さ**れます。MessageManager**メッセージ。 
  
## <a name="remarks"></a>解説

**PR_CONVERSATION_KEY**プロパティは、 **PR_CONVERSATION_INDEX**、 [PidTagConversationIndex 標準プロパティ](pidtagconversationindex-canonical-property.md)、 **PR_CONVERSATION_TOPIC**、PidTagConversationTopic 標準の precursor のうち、使用されていないものです。 [プロパティ](pidtagconversationtopic-canonical-property.md)。代わりに使用する必要があります。
  
## <a name="see-also"></a>関連項目

- [IPM サブツリー](ipm-subtree.md)
- [MAPI の特殊フォルダー](mapi-special-folders.md)

