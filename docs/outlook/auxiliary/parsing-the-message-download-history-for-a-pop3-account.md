---
title: POP3 アカウントのメッセージ ダウンロード履歴の解析
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: このトピックでは、pop3 アカウントのメッセージのダウンロード履歴を表す pop3 BLOB の構造について説明し、そのアカウントでダウンロードまたは削除されたメッセージを識別します。
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327766"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a><span data-ttu-id="8d8f3-103">POP3 アカウントのメッセージ ダウンロード履歴の解析</span><span class="sxs-lookup"><span data-stu-id="8d8f3-103">Parsing the message download history for a POP3 account</span></span>

<span data-ttu-id="8d8f3-104">このトピックでは、pop3 アカウントのメッセージのダウンロード履歴を表す pop3 BLOB の構造について説明し、そのアカウントでダウンロードまたは削除されたメッセージを識別します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-104">This topic describes the structure of the POP3 BLOB that represents the message download history of a POP3 account, to identify the messages that have been downloaded or deleted on that account.</span></span>

<span data-ttu-id="8d8f3-105"><a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a></span><span class="sxs-lookup"><span data-stu-id="8d8f3-105"></span></span>

## <a name="why-parse-the-message-download-history"></a><span data-ttu-id="8d8f3-106">メッセージのダウンロード履歴を解析する理由</span><span class="sxs-lookup"><span data-stu-id="8d8f3-106">Why parse the message download history?</span></span>

<span data-ttu-id="8d8f3-107">Outlook の Post Office Protocol (POP) プロバイダーを使用すると、ユーザーは新しい電子メールメッセージをローカルデバイスで取得してダウンロードし、メールサーバー上でこれらの電子メールメッセージを残すか削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-107">The Post Office Protocol (POP) provider for Outlook allows users to retrieve and download new email messages on their local device, and subsequently to leave or delete these email messages on the mail server.</span></span> <span data-ttu-id="8d8f3-108">メールクライアントは、新しいメッセージのダウンロードを確認するときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-108">When the mail client checks for new messages to download, it has to be able to identify and download only the new messages for that Inbox.</span></span> <span data-ttu-id="8d8f3-109">メールクライアントは、最初に UIDL (Unique ID リスト) コマンドを使用して、その受信トレイに配信された各メッセージのマップを一意の識別子 (UID) に取得します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-109">The mail client does this by first using the UIDL (Unique ID Listing) command to obtain a map of each message that has ever been delivered to that Inbox to a unique identifier (UID).</span></span> <span data-ttu-id="8d8f3-110">クライアントは、そのクライアント上で受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-110">The client also gets the message download history for messages that have been downloaded or deleted for the Inbox on that client.</span></span> <span data-ttu-id="8d8f3-111">メッセージ UID マップとダウンロード履歴を使用して、クライアントは、履歴に存在しないメッセージを新規として識別できるため、ダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-111">Using the message UID map and download history, the client can then identify those messages that are absent from the history as new and, hence, should be downloaded.</span></span>
  
<span data-ttu-id="8d8f3-112">受信トレイのメッセージダウンロード履歴を取得するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-112">To get the messages download history for an Inbox:</span></span>
  
- <span data-ttu-id="8d8f3-113">pop3 アカウントのメッセージ[のダウンロード履歴](locating-the-message-download-history-for-a-pop3-account.md)を探す手順に従って、 [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティを検索します。このプロパティには、pop3 アカウントのメッセージ履歴を表すバイナリラージオブジェクト (BLOB) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-113">Follow the steps in [Locating the message download history for a POP3 account](locating-the-message-download-history-for-a-pop3-account.md) to find the [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) property, which contains a binary large object (BLOB) that represents the message history for a POP3 account.</span></span> 
    
- <span data-ttu-id="8d8f3-114">このトピックでは、blob の構造について説明し、POP3 アカウントの受信トレイでダウンロードまたは削除されたメッセージを識別するための blob の例を示します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-114">Read this topic, which describes the structure of the BLOB, and shows an example BLOB to identify messages that have been downloaded or deleted for the Inbox of the POP3 account.</span></span>

<span data-ttu-id="8d8f3-115"><a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a></span><span class="sxs-lookup"><span data-stu-id="8d8f3-115"></span></span>

## <a name="pop-blob-structure"></a><span data-ttu-id="8d8f3-116">POP BLOB 構造</span><span class="sxs-lookup"><span data-stu-id="8d8f3-116">POP BLOB structure</span></span>

<span data-ttu-id="8d8f3-117">表1で説明されているように、POP BLOB 構造は、**バージョン**と**数**の2つの\*\*\*\* フィールドで始まり、その後にリソースタグの数が続き、それぞれが null で終わります。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-117">The POP BLOB structure, as described in Table 1, begins with two fields, **Version** and **Count**, followed by a **Count** number of resource tags, each of which is null-terminated.</span></span> 
  
<span data-ttu-id="8d8f3-118">**表1POP3 アカウントのメッセージダウンロード履歴を表す BLOB の構造**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-118">**Table 1. Structure of the BLOB that represents the message download history of a POP3 account**</span></span>

|<span data-ttu-id="8d8f3-119">**BLOB のフィールド**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-119">**Field in BLOB**</span></span>|<span data-ttu-id="8d8f3-120">**Size**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-120">**Size**</span></span>|<span data-ttu-id="8d8f3-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d8f3-122">**バージョン**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-122">**Version**</span></span> <br/> |<span data-ttu-id="8d8f3-123">2 バイト</span><span class="sxs-lookup"><span data-stu-id="8d8f3-123">2 bytes</span></span>  <br/> |<span data-ttu-id="8d8f3-124">3 (**PBLOB_VERSION_NUM**) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-124">Must be 3 (**PBLOB_VERSION_NUM**).</span></span>  <br/> |
|<span data-ttu-id="8d8f3-125">**Count**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-125">**Count**</span></span> <br/> |<span data-ttu-id="8d8f3-126">2 バイト</span><span class="sxs-lookup"><span data-stu-id="8d8f3-126">2 bytes</span></span>  <br/> |<span data-ttu-id="8d8f3-127">この BLOB 内のリソースタグの数。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-127">The number of resource tags in this BLOB.</span></span>  <br/> |
|<span data-ttu-id="8d8f3-128">リソースタグ</span><span class="sxs-lookup"><span data-stu-id="8d8f3-128">Resource tag</span></span>  <br/> |<span data-ttu-id="8d8f3-129">可変</span><span class="sxs-lookup"><span data-stu-id="8d8f3-129">Variable</span></span>  <br/> |<span data-ttu-id="8d8f3-130">リソースタグをエンコードする0個以上の null で終了する utf-8 文字列。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-130">0 or more null-terminated UTF-8 strings that encode the resource tags.</span></span> <span data-ttu-id="8d8f3-131">null で終わる文字列の数は、 **Count**と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-131">The number of null-terminated strings must match **Count**.</span></span>  <br/> |
   
<span data-ttu-id="8d8f3-132">各リソースタグは、メッセージに適用される操作、操作に関する日付時メタデータ、およびメッセージの UID をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-132">Each resource tag specifies the operation that is applied to a message, some date-time metadata about the operation, and encodes the UID of the message.</span></span> <span data-ttu-id="8d8f3-133">リソースタグ文字列の形式は、次のように分割されており、表2でさらに詳しく説明されています。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-133">The format of a resource tag string is broken down as follows, and is further explained in Table 2.</span></span> 
  
`Ocyyyymmddhhmmssuuu...`
  
<span data-ttu-id="8d8f3-134">**表2リソースタグの構造**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-134">**Table 2. Structure of a resource tag**</span></span>

|<span data-ttu-id="8d8f3-135">**リソースタグのフィールド**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-135">**Field in a resource tag**</span></span>|<span data-ttu-id="8d8f3-136">**Size**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-136">**Size**</span></span>|<span data-ttu-id="8d8f3-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-137">**Description**</span></span>|
|:-----|:-----|:-----|
| `O` <br/> |<span data-ttu-id="8d8f3-138">1文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-138">1 character</span></span>  <br/> |<span data-ttu-id="8d8f3-139">電子メールメッセージに対して実行された操作。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-139">The operation performed on the email message.</span></span> <span data-ttu-id="8d8f3-140">この値は、"+"、"-"、または&amp;"" のいずれかである必要があります。この値は、それぞれ、get、delete、または取得操作が正常に行われたことを示します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-140">The value must be "+", "-", or "&amp;", which indicates a successful get, delete, or get-and-delete operation, respectively.</span></span>  <br/> |
| `c` <br/> |<span data-ttu-id="8d8f3-141">1文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-141">1 character</span></span>  <br/> |<span data-ttu-id="8d8f3-142">操作に関係するメッセージコンテンツの一部。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-142">The part of the message content involved in the operation.</span></span> <span data-ttu-id="8d8f3-143">値は、""、"h"、または "b" のいずれかである必要があります。この値は、それぞれ none、header、または body の内容を示します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-143">The value must be " ", "h", or "b", which indicates the content of none, header, or body, respectively.</span></span>  <br/> |
| `yyyy` <br/> |<span data-ttu-id="8d8f3-144">4文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-144">4 characters</span></span>  <br/> |<span data-ttu-id="8d8f3-145">操作の4桁の年。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-145">The four-digit year of the operation.</span></span>  <br/> |
| `MM` <br/> |<span data-ttu-id="8d8f3-146">2文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-146">2 characters</span></span>  <br/> |<span data-ttu-id="8d8f3-147">操作の2桁の月を示します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-147">The two-digit month of the operation.</span></span>  <br/> |
| `dd` <br/> |<span data-ttu-id="8d8f3-148">2文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-148">2 characters</span></span>  <br/> |<span data-ttu-id="8d8f3-149">操作の2桁の日。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-149">The two-digit day of the operation.</span></span>  <br/> |
| `hh` <br/> |<span data-ttu-id="8d8f3-150">2文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-150">2 characters</span></span>  <br/> |<span data-ttu-id="8d8f3-151">操作の2桁の時間。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-151">The two-digit hour of the operation.</span></span>  <br/> |
| `mm` <br/> |<span data-ttu-id="8d8f3-152">2文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-152">2 characters</span></span>  <br/> |<span data-ttu-id="8d8f3-153">操作の2桁の分。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-153">The two-digit minute of the operation.</span></span>  <br/> |
| `ss` <br/> |<span data-ttu-id="8d8f3-154">2文字</span><span class="sxs-lookup"><span data-stu-id="8d8f3-154">2 characters</span></span>  <br/> |<span data-ttu-id="8d8f3-155">操作の2桁の秒。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-155">The two-digit second of the operation.</span></span>  <br/> |
| `uuu…` <br/> |<span data-ttu-id="8d8f3-156">可変長</span><span class="sxs-lookup"><span data-stu-id="8d8f3-156">Variable length</span></span>  <br/> |<span data-ttu-id="8d8f3-157">メッセージのエンコードされた UID。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-157">The encoded UID of a message.</span></span>  <br/> |

<span data-ttu-id="8d8f3-158"><a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="8d8f3-158"></span></span>

## <a name="example"></a><span data-ttu-id="8d8f3-159">例</span><span class="sxs-lookup"><span data-stu-id="8d8f3-159">Example</span></span>

<span data-ttu-id="8d8f3-160">図1は、POP アカウントのメッセージのダウンロード履歴を表す BLOB の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-160">Figure 1 shows an example of a BLOB that represents the message download history of a POP account.</span></span> 
  
<span data-ttu-id="8d8f3-161">**図1。POP3 アカウントのメッセージダウンロード履歴の BLOB 構造の例**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-161">**Figure 1. Example BLOB structure for the message download history of a POP3 account**</span></span>

![POP3 アカウントのメッセージ ダウンロード履歴の BLOB](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
<span data-ttu-id="8d8f3-163">表1と表2に記載されている構造に基づいて、この BLOB は23件の電子メールメッセージのダウンロード履歴を表します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-163">Based on the structure described in Table 1 and Table 2, this BLOB represents the download history of 23 email messages.</span></span>
  
<span data-ttu-id="8d8f3-164">各リソースタグの生の uid を解析するには、uid がこのエンコーディングに従っていることに注意してください。 uid 内の文字は大部分が英数字で、各英数字以外の文字の前には ASCII 文字の "$" (0x24) が付けられます。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-164">To parse the raw UID in each resource tag, be aware that the UID follows this encoding: characters in a UID are mostly alphanumeric characters, and each non-alphanumeric character is preceded by the ASCII character "$" (0x24).</span></span> <span data-ttu-id="8d8f3-165">そのため、ASCII 文字 $ 2d は英数字以外の文字 "-" を表します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-165">So the ASCII characters $2d represent the non-alphanumeric character "-".</span></span> <span data-ttu-id="8d8f3-166">図2では、最初にリソースタグ1の生の UID を ASCII 表記に変換し、次に英数字以外の文字を "$" の前に変換して、実際の uid を生成する例を示します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-166">Figure 2 shows an example of first converting the raw UID in resource tag 1 to the ASCII representation, then converting any non-alphanumeric character preceded by "$" to produce the actual UID:</span></span>
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
<span data-ttu-id="8d8f3-167">**図2リソースタグ内の生の uid を実際のメッセージ uid に変換する**</span><span class="sxs-lookup"><span data-stu-id="8d8f3-167">**Figure 2. Converting the raw UID in a resource tag to the actual message UID**</span></span>

![BLOB の生の UID から実際のメッセージ UID への変換](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
<span data-ttu-id="8d8f3-169">この BLOB 内のリソースタグ1を解釈するには、2012 `0BC535DB-EA63-11E1-A75C-00215AD7BB74`年9月6日に、UID を持つメッセージが13:11:38 に正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-169">To interpret resource tag 1 in this BLOB: the message with the UID  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` was successfully retrieved on September 6, 2012, at 13:11:38.</span></span> 
  
<span data-ttu-id="8d8f3-170">同様に、その BLOB の残りの22個のリソースタグを解析することもできます。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-170">You can similarly parse the remaining 22 resource tags for that BLOB.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d8f3-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d8f3-171">See also</span></span>
<span data-ttu-id="8d8f3-172"><a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a></span><span class="sxs-lookup"><span data-stu-id="8d8f3-172"></span></span>

- [<span data-ttu-id="8d8f3-173">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="8d8f3-173">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)    
- [<span data-ttu-id="8d8f3-174">POP3 アカウントのメッセージのダウンロードの履歴を検索します。</span><span class="sxs-lookup"><span data-stu-id="8d8f3-174">Locating the message download history for a POP3 account</span></span>](locating-the-message-download-history-for-a-pop3-account.md)    
- [<span data-ttu-id="8d8f3-175">POP3 の UIDL 履歴の解析</span><span class="sxs-lookup"><span data-stu-id="8d8f3-175">Parsing the POP3 UIDL History</span></span>](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

