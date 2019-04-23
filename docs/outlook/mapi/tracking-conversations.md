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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706222"
---
# <a name="tracking-conversations"></a><span data-ttu-id="bd0dc-103">会話の追跡</span><span class="sxs-lookup"><span data-stu-id="bd0dc-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="bd0dc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd0dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd0dc-p101">会話の追跡とは、メッセージに対する応答を収集することです。クライアントでは、会話の追跡に役立つ次の 2 つのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="bd0dc-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd0dc-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="bd0dc-108">**PR_CONVERSATION_TOPIC** は、メッセージの正規化された件名 (プレフィックス文字列のない件名) です。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings. Set this property to the value of the message's PR_NORMALIZED_SUBJECT ( PidTagNormalizedSubject) property.</span></span> <span data-ttu-id="bd0dc-109">このプロパティは、メッセージの **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) プロパティの値に設定します。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="bd0dc-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd0dc-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="bd0dc-p103">\*\* PR_CONVERSATION_INDEX **は特定の会話内のメッセージの位置を示します。新しいメッセージ、転送されたメッセージ、返信のいずれであっても、各発信メッセージに** PR_CONVERSATION_INDEX \*\*を設定することはクライアントの管轄です。クライアントはこのプロパティを手動で設定するか、MAPIが提供するユーティリティー機能である[ ScCreateConversationIndex ](sccreateconversationindex.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="bd0dc-p104">\*\* ScCreateConversationIndex \*\*は、発信メッセージの会話インデックスの値を生成します。 \*\* ScCreateConversationIndex \*\*は、インデックスを長さ22バイトのヘッダーブロックとして実装し、その後に長さが5バイトずつ、ゼロ個以上の子ブロックを続けます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="bd0dc-116">ヘッダブロックは22バイトで構成され、3つの部分に分けられます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="bd0dc-p105">保存されたバイト。値は1です。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="bd0dc-119">[FILETIME](filetime.md)構造形式に変換された現在のシステム時刻の5バイト。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="bd0dc-120">16 バイトを保持する [GUID](guid.md) (グローバル一意識別子)。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="bd0dc-121">各子ブロックは5バイトで構成され、次のように分割されています。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="bd0dc-p106">現在の時刻とヘッダーブロックに格納されている時刻との差を表すコードを含む1ビット。このビットは、差が0.02秒未満で2年以上の場合は0、差が1秒未満で56年以上の場合は1になります。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="bd0dc-p107">現在の時刻と\*\* FILETIME **単位で表されるヘッダブロックの時刻の差を含む31ビット。子ブロックのこの部分は、最初のビットの値に応じて、2つの方法のうちの1つを使用して生成されます。 このビットがゼロの場合、** ScCreateConversationIndex \*\*は上位15ビットと下位18ビットを破棄します。このビットが1の場合、このコードは上位10ビットと下位23ビットを破棄します。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="bd0dc-127">Win32関数[ GetTickCount ](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx)を呼び出して生成された乱数を含む4ビット。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="bd0dc-128">乱数の一部から取られたシーケンス数を含む4ビット。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="bd0dc-129">メッセージの会話インデックスを手動で設定することを選択した場合は、以下の事項を検討してください。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="bd0dc-130">回答者のタイムゾーンの違いをはっきりさせる。現地時間ではなくUTC時間を使用する。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="bd0dc-131">各会話グループを同じ量だけインデントする。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="bd0dc-132">同じメッセージ日付への返答は整理する。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="bd0dc-133">別々の時間に立てられた別々のスレッドが、偶然同じトピックを共有しました。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="bd0dc-134">メッセージがトピックごとにグループ化されるようにする分類別の並べ替えを実装するには、最初に **PR_CONVERSATION_TOPIC** で並べ替えてから、**PR_CONVERSATION_INDEX** で並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="bd0dc-135">並べ替えの結果を表示するには、22 バイト長の会話インデックスを持つメッセージの **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="bd0dc-136">その後で、5 バイト長ずつ増加するたびに、**PR_DEPTH** プロパティの値を 1 増やします。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="bd0dc-137">プロパティの PR_ORIGINAL グループは、会話の追跡にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="bd0dc-138">これらのプロパティを設定して、元のメッセージへの返信メッセージまたは転送メッセージをリンクします。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="bd0dc-139">PR_ORIGINAL のすべてのプロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="bd0dc-140">たとえば、**PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)) を明示的に設定していない場合、メッセージ ストア プロバイダーは既定の値 (**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティの値) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="bd0dc-141">同様に、**PR_ORIGINAL_AUTHOR_NAME** または **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) を設定していない場合、これらのプロパティには、**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティと **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティの値がそれぞれの既定値として設定されます。</span><span class="sxs-lookup"><span data-stu-id="bd0dc-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

