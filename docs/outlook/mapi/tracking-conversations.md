---
title: 会話の追跡
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '最終更新日: 2011 年 7 月 23 日'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349547"
---
# <a name="tracking-conversations"></a>会話の追跡

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会話の追跡とは、メッセージに対する応答を収集することです。クライアントでは、会話の追跡に役立つ次の 2 つのプロパティを設定する必要があります。
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** は、メッセージの正規化された件名 (プレフィックス文字列のない件名) です。 このプロパティは、メッセージの **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) プロパティの値に設定します。 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    ** PR_CONVERSATION_INDEX **は特定の会話内のメッセージの位置を示します。新しいメッセージ、転送されたメッセージ、返信のいずれであっても、各発信メッセージに** PR_CONVERSATION_INDEX **を設定することはクライアントの管轄です。クライアントはこのプロパティを手動で設定するか、MAPIが提供するユーティリティー機能である[ ScCreateConversationIndex ](sccreateconversationindex.md)を呼び出すことができます。 
    
 ** ScCreateConversationIndex **は、発信メッセージの会話インデックスの値を生成します。 ** ScCreateConversationIndex **は、インデックスを長さ22バイトのヘッダーブロックとして実装し、その後に長さが5バイトずつ、ゼロ個以上の子ブロックを続けます。 
  
ヘッダブロックは22バイトで構成され、3つの部分に分けられます。
  
- 保存されたバイト。値は1です。
    
- [FILETIME](filetime.md)構造形式に変換された現在のシステム時刻の5バイト。 
    
- 16 バイトを保持する [GUID](guid.md) (グローバル一意識別子)。
    
各子ブロックは5バイトで構成され、次のように分割されています。
  
- 現在の時刻とヘッダーブロックに格納されている時刻との差を表すコードを含む1ビット。このビットは、差が0.02秒未満で2年以上の場合は0、差が1秒未満で56年以上の場合は1になります。
    
- 現在の時刻と** FILETIME **単位で表されるヘッダブロックの時刻の差を含む31ビット。子ブロックのこの部分は、最初のビットの値に応じて、2つの方法のうちの1つを使用して生成されます。 このビットがゼロの場合、** ScCreateConversationIndex **は上位15ビットと下位18ビットを破棄します。このビットが1の場合、このコードは上位10ビットと下位23ビットを破棄します。 
    
- Win32関数[ GetTickCount ](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx)を呼び出して生成された乱数を含む4ビット。
    
- 乱数の一部から取られたシーケンス数を含む4ビット。
    
メッセージの会話インデックスを手動で設定することを選択した場合は、以下の事項を検討してください。
  
1. 回答者のタイムゾーンの違いをはっきりさせる。現地時間ではなくUTC時間を使用する。
    
2. 各会話グループを同じ量だけインデントする。
    
3. 同じメッセージ日付への返答は整理する。
    
4. 別々の時間に立てられた別々のスレッドが、偶然同じトピックを共有しました。 
    
5. メッセージがトピックごとにグループ化されるようにする分類別の並べ替えを実装するには、最初に **PR_CONVERSATION_TOPIC** で並べ替えてから、**PR_CONVERSATION_INDEX** で並べ替えます。 並べ替えの結果を表示するには、22 バイト長の会話インデックスを持つメッセージの **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを 0 に設定します。 その後で、5 バイト長ずつ増加するたびに、**PR_DEPTH** プロパティの値を 1 増やします。 
    
プロパティの PR_ORIGINAL グループは、会話の追跡にも使用できます。 これらのプロパティを設定して、元のメッセージへの返信メッセージまたは転送メッセージをリンクします。 PR_ORIGINAL のすべてのプロパティは省略可能です。 たとえば、**PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)) を明示的に設定していない場合、メッセージ ストア プロバイダーは既定の値 (**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティの値) を使用できます。 同様に、**PR_ORIGINAL_AUTHOR_NAME** または **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) を設定していない場合、これらのプロパティには、**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティと **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティの値がそれぞれの既定値として設定されます。 
  

