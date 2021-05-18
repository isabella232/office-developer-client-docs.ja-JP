---
title: POP3 アカウントのメッセージ ダウンロード履歴の解析
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: このトピックでは、そのアカウントでダウンロードまたは削除されたメッセージを識別するために、POP3 アカウントのメッセージダウンロード履歴を表す POP3 BLOB の構造について説明します。
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327766"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a><span data-ttu-id="30153-103">POP3 アカウントのメッセージ ダウンロード履歴の解析</span><span class="sxs-lookup"><span data-stu-id="30153-103">Parsing the message download history for a POP3 account</span></span>

<span data-ttu-id="30153-104">このトピックでは、そのアカウントでダウンロードまたは削除されたメッセージを識別するために、POP3 アカウントのメッセージダウンロード履歴を表す POP3 BLOB の構造について説明します。</span><span class="sxs-lookup"><span data-stu-id="30153-104">This topic describes the structure of the POP3 BLOB that represents the message download history of a POP3 account, to identify the messages that have been downloaded or deleted on that account.</span></span>

<span data-ttu-id="30153-105"><a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a></span><span class="sxs-lookup"><span data-stu-id="30153-105"><a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a></span></span>

## <a name="why-parse-the-message-download-history"></a><span data-ttu-id="30153-106">メッセージのダウンロード履歴を解析する理由</span><span class="sxs-lookup"><span data-stu-id="30153-106">Why parse the message download history?</span></span>

<span data-ttu-id="30153-107">Outlook の post Office プロトコル (POP) プロバイダーを使用すると、ユーザーはローカル デバイス上の新しい電子メール メッセージを取得してダウンロードし、その後、メール サーバー上でこれらの電子メール メッセージを残したり削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="30153-107">The Post Office Protocol (POP) provider for Outlook allows users to retrieve and download new email messages on their local device, and subsequently to leave or delete these email messages on the mail server.</span></span> <span data-ttu-id="30153-108">メール クライアントは、ダウンロードする新しいメッセージをチェックするときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="30153-108">When the mail client checks for new messages to download, it has to be able to identify and download only the new messages for that Inbox.</span></span> <span data-ttu-id="30153-109">メール クライアントは、まず UIDL (Unique ID Listing) コマンドを使用して、その受信トレイに一意の識別子 (UID) に配信された各メッセージのマップを取得します。</span><span class="sxs-lookup"><span data-stu-id="30153-109">The mail client does this by first using the UIDL (Unique ID Listing) command to obtain a map of each message that has ever been delivered to that Inbox to a unique identifier (UID).</span></span> <span data-ttu-id="30153-110">クライアントは、そのクライアントの受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。</span><span class="sxs-lookup"><span data-stu-id="30153-110">The client also gets the message download history for messages that have been downloaded or deleted for the Inbox on that client.</span></span> <span data-ttu-id="30153-111">メッセージ UID マップとダウンロード履歴を使用して、クライアントは履歴から存在しないメッセージを新しいメッセージとして識別し、したがってダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="30153-111">Using the message UID map and download history, the client can then identify those messages that are absent from the history as new and, hence, should be downloaded.</span></span>
  
<span data-ttu-id="30153-112">受信トレイのメッセージダウンロード履歴を取得するには、次の方法を実行します。</span><span class="sxs-lookup"><span data-stu-id="30153-112">To get the messages download history for an Inbox:</span></span>
  
- <span data-ttu-id="30153-113">[「POP3](locating-the-message-download-history-for-a-pop3-account.md)アカウントのメッセージダウンロード履歴を検索する」の手順に従って、POP3 アカウントのメッセージ履歴を表すバイナリ ラージ オブジェクト (BLOB) を含む[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="30153-113">Follow the steps in [Locating the message download history for a POP3 account](locating-the-message-download-history-for-a-pop3-account.md) to find the [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) property, which contains a binary large object (BLOB) that represents the message history for a POP3 account.</span></span> 
    
- <span data-ttu-id="30153-114">このトピックでは、BLOB の構造について説明し、POP3 アカウントの受信トレイに対してダウンロードまたは削除されたメッセージを識別するための BLOB の例を示します。</span><span class="sxs-lookup"><span data-stu-id="30153-114">Read this topic, which describes the structure of the BLOB, and shows an example BLOB to identify messages that have been downloaded or deleted for the Inbox of the POP3 account.</span></span>

<span data-ttu-id="30153-115"><a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a></span><span class="sxs-lookup"><span data-stu-id="30153-115"><a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a></span></span>

## <a name="pop-blob-structure"></a><span data-ttu-id="30153-116">POP BLOB 構造</span><span class="sxs-lookup"><span data-stu-id="30153-116">POP BLOB structure</span></span>

<span data-ttu-id="30153-117">表 1 で説明されている POP BLOB 構造は、Versionと **Count** の 2つのフィールドから始まり、その後に Count のリソース タグの数が続き、それぞれが null で終了します。</span><span class="sxs-lookup"><span data-stu-id="30153-117">The POP BLOB structure, as described in Table 1, begins with two fields, **Version** and **Count**, followed by a **Count** number of resource tags, each of which is null-terminated.</span></span> 
  
<span data-ttu-id="30153-118">**表 1.POP3 アカウントのメッセージダウンロード履歴を表す BLOB の構造**</span><span class="sxs-lookup"><span data-stu-id="30153-118">**Table 1. Structure of the BLOB that represents the message download history of a POP3 account**</span></span>

|<span data-ttu-id="30153-119">**BLOB のフィールド**</span><span class="sxs-lookup"><span data-stu-id="30153-119">**Field in BLOB**</span></span>|<span data-ttu-id="30153-120">**[サイズ]**</span><span class="sxs-lookup"><span data-stu-id="30153-120">**Size**</span></span>|<span data-ttu-id="30153-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="30153-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30153-122">**バージョン**</span><span class="sxs-lookup"><span data-stu-id="30153-122">**Version**</span></span> <br/> |<span data-ttu-id="30153-123">2 バイト</span><span class="sxs-lookup"><span data-stu-id="30153-123">2 bytes</span></span>  <br/> |<span data-ttu-id="30153-124">3 ( PBLOB_VERSION_NUM )**である必要があります**。</span><span class="sxs-lookup"><span data-stu-id="30153-124">Must be 3 (**PBLOB_VERSION_NUM**).</span></span>  <br/> |
|<span data-ttu-id="30153-125">**Count**</span><span class="sxs-lookup"><span data-stu-id="30153-125">**Count**</span></span> <br/> |<span data-ttu-id="30153-126">2 バイト</span><span class="sxs-lookup"><span data-stu-id="30153-126">2 bytes</span></span>  <br/> |<span data-ttu-id="30153-127">この BLOB 内のリソース タグの数。</span><span class="sxs-lookup"><span data-stu-id="30153-127">The number of resource tags in this BLOB.</span></span>  <br/> |
|<span data-ttu-id="30153-128">リソース タグ</span><span class="sxs-lookup"><span data-stu-id="30153-128">Resource tag</span></span>  <br/> |<span data-ttu-id="30153-129">変数</span><span class="sxs-lookup"><span data-stu-id="30153-129">Variable</span></span>  <br/> |<span data-ttu-id="30153-130">リソース タグをエンコードする 0 UTF-8 null 終端文字列。</span><span class="sxs-lookup"><span data-stu-id="30153-130">0 or more null-terminated UTF-8 strings that encode the resource tags.</span></span> <span data-ttu-id="30153-131">null 終端文字列の数は Count と一致する **必要があります**。</span><span class="sxs-lookup"><span data-stu-id="30153-131">The number of null-terminated strings must match **Count**.</span></span>  <br/> |
   
<span data-ttu-id="30153-132">各リソース タグは、メッセージに適用される操作、操作に関する日時のメタデータを指定し、メッセージの UID をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="30153-132">Each resource tag specifies the operation that is applied to a message, some date-time metadata about the operation, and encodes the UID of the message.</span></span> <span data-ttu-id="30153-133">リソース タグ文字列の形式は次のように分解され、表 2 でさらに説明します。</span><span class="sxs-lookup"><span data-stu-id="30153-133">The format of a resource tag string is broken down as follows, and is further explained in Table 2.</span></span> 
  
`Ocyyyymmddhhmmssuuu...`
  
<span data-ttu-id="30153-134">**表 2.リソース タグの構造**</span><span class="sxs-lookup"><span data-stu-id="30153-134">**Table 2. Structure of a resource tag**</span></span>

|<span data-ttu-id="30153-135">**リソース タグのフィールド**</span><span class="sxs-lookup"><span data-stu-id="30153-135">**Field in a resource tag**</span></span>|<span data-ttu-id="30153-136">**[サイズ]**</span><span class="sxs-lookup"><span data-stu-id="30153-136">**Size**</span></span>|<span data-ttu-id="30153-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="30153-137">**Description**</span></span>|
|:-----|:-----|:-----|
| `O` <br/> |<span data-ttu-id="30153-138">1 文字</span><span class="sxs-lookup"><span data-stu-id="30153-138">1 character</span></span>  <br/> |<span data-ttu-id="30153-139">電子メール メッセージに対して実行された操作。</span><span class="sxs-lookup"><span data-stu-id="30153-139">The operation performed on the email message.</span></span> <span data-ttu-id="30153-140">値は"+"、"-"、または ""である必要があります。これは、それぞれ正常な取得、削除、または &amp; get-and-delete 操作を示します。</span><span class="sxs-lookup"><span data-stu-id="30153-140">The value must be "+", "-", or "&amp;", which indicates a successful get, delete, or get-and-delete operation, respectively.</span></span>  <br/> |
| `c` <br/> |<span data-ttu-id="30153-141">1 文字</span><span class="sxs-lookup"><span data-stu-id="30153-141">1 character</span></span>  <br/> |<span data-ttu-id="30153-142">操作に関係するメッセージ コンテンツの部分。</span><span class="sxs-lookup"><span data-stu-id="30153-142">The part of the message content involved in the operation.</span></span> <span data-ttu-id="30153-143">値は"、"h"、または "b" である必要があります。これは、それぞれ none、ヘッダー、または本文の内容を示します。</span><span class="sxs-lookup"><span data-stu-id="30153-143">The value must be " ", "h", or "b", which indicates the content of none, header, or body, respectively.</span></span>  <br/> |
| `yyyy` <br/> |<span data-ttu-id="30153-144">4 文字</span><span class="sxs-lookup"><span data-stu-id="30153-144">4 characters</span></span>  <br/> |<span data-ttu-id="30153-145">操作の 4 桁の年。</span><span class="sxs-lookup"><span data-stu-id="30153-145">The four-digit year of the operation.</span></span>  <br/> |
| `MM` <br/> |<span data-ttu-id="30153-146">2 文字</span><span class="sxs-lookup"><span data-stu-id="30153-146">2 characters</span></span>  <br/> |<span data-ttu-id="30153-147">操作の 2 桁の月。</span><span class="sxs-lookup"><span data-stu-id="30153-147">The two-digit month of the operation.</span></span>  <br/> |
| `dd` <br/> |<span data-ttu-id="30153-148">2 文字</span><span class="sxs-lookup"><span data-stu-id="30153-148">2 characters</span></span>  <br/> |<span data-ttu-id="30153-149">操作の 2 桁の日。</span><span class="sxs-lookup"><span data-stu-id="30153-149">The two-digit day of the operation.</span></span>  <br/> |
| `hh` <br/> |<span data-ttu-id="30153-150">2 文字</span><span class="sxs-lookup"><span data-stu-id="30153-150">2 characters</span></span>  <br/> |<span data-ttu-id="30153-151">操作の 2 桁の時間。</span><span class="sxs-lookup"><span data-stu-id="30153-151">The two-digit hour of the operation.</span></span>  <br/> |
| `mm` <br/> |<span data-ttu-id="30153-152">2 文字</span><span class="sxs-lookup"><span data-stu-id="30153-152">2 characters</span></span>  <br/> |<span data-ttu-id="30153-153">操作の 2 桁の分。</span><span class="sxs-lookup"><span data-stu-id="30153-153">The two-digit minute of the operation.</span></span>  <br/> |
| `ss` <br/> |<span data-ttu-id="30153-154">2 文字</span><span class="sxs-lookup"><span data-stu-id="30153-154">2 characters</span></span>  <br/> |<span data-ttu-id="30153-155">操作の 2 桁の秒。</span><span class="sxs-lookup"><span data-stu-id="30153-155">The two-digit second of the operation.</span></span>  <br/> |
| `uuu…` <br/> |<span data-ttu-id="30153-156">可変長</span><span class="sxs-lookup"><span data-stu-id="30153-156">Variable length</span></span>  <br/> |<span data-ttu-id="30153-157">メッセージのエンコードされた UID。</span><span class="sxs-lookup"><span data-stu-id="30153-157">The encoded UID of a message.</span></span>  <br/> |

<span data-ttu-id="30153-158"><a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="30153-158"><a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a></span></span>

## <a name="example"></a><span data-ttu-id="30153-159">例</span><span class="sxs-lookup"><span data-stu-id="30153-159">Example</span></span>

<span data-ttu-id="30153-160">図 1 は、POP アカウントのメッセージダウンロード履歴を表す BLOB の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="30153-160">Figure 1 shows an example of a BLOB that represents the message download history of a POP account.</span></span> 
  
<span data-ttu-id="30153-161">**図 1.POP3 アカウントのメッセージダウンロード履歴の BLOB 構造の例**</span><span class="sxs-lookup"><span data-stu-id="30153-161">**Figure 1. Example BLOB structure for the message download history of a POP3 account**</span></span>

![POP3 アカウントのメッセージ ダウンロード履歴の BLOB](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
<span data-ttu-id="30153-163">表 1 と表 2 に記載されている構造に基づいて、この BLOB は 23 の電子メール メッセージのダウンロード履歴を表します。</span><span class="sxs-lookup"><span data-stu-id="30153-163">Based on the structure described in Table 1 and Table 2, this BLOB represents the download history of 23 email messages.</span></span>
  
<span data-ttu-id="30153-164">各リソース タグで生の UID を解析するには、UID は次のエンコードに従います。UID の文字は主に英数字で、英数字以外の各文字の前には ASCII 文字 "$" (0x24) が付きます。</span><span class="sxs-lookup"><span data-stu-id="30153-164">To parse the raw UID in each resource tag, be aware that the UID follows this encoding: characters in a UID are mostly alphanumeric characters, and each non-alphanumeric character is preceded by the ASCII character "$" (0x24).</span></span> <span data-ttu-id="30153-165">したがって、ASCII 文字 $2d は英数字以外の文字 "-" を表します。</span><span class="sxs-lookup"><span data-stu-id="30153-165">So the ASCII characters $2d represent the non-alphanumeric character "-".</span></span> <span data-ttu-id="30153-166">図 2 は、最初にリソース タグ 1 の生 UID を ASCII 表記に変換し、その後に"$" の前に英数字以外の文字を変換して実際の UID を生成する例を示しています。</span><span class="sxs-lookup"><span data-stu-id="30153-166">Figure 2 shows an example of first converting the raw UID in resource tag 1 to the ASCII representation, then converting any non-alphanumeric character preceded by "$" to produce the actual UID:</span></span>
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
<span data-ttu-id="30153-167">**図 2.リソース タグの生 UID を実際のメッセージ UID に変換する**</span><span class="sxs-lookup"><span data-stu-id="30153-167">**Figure 2. Converting the raw UID in a resource tag to the actual message UID**</span></span>

![BLOB の生の UID から実際のメッセージ UID への変換](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
<span data-ttu-id="30153-169">この BLOB のリソース タグ 1 を解釈するには、UID を含むメッセージが  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` 2012 年 9 月 6 日 13:11:38 に正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="30153-169">To interpret resource tag 1 in this BLOB: the message with the UID  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` was successfully retrieved on September 6, 2012, at 13:11:38.</span></span> 
  
<span data-ttu-id="30153-170">同様に、その BLOB の残りの 22 のリソース タグを解析できます。</span><span class="sxs-lookup"><span data-stu-id="30153-170">You can similarly parse the remaining 22 resource tags for that BLOB.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30153-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="30153-171">See also</span></span>
<span data-ttu-id="30153-172"><a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a></span><span class="sxs-lookup"><span data-stu-id="30153-172"><a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a></span></span>

- [<span data-ttu-id="30153-173">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="30153-173">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)    
- [<span data-ttu-id="30153-174">POP3 アカウントのメッセージのダウンロードの履歴を検索します。</span><span class="sxs-lookup"><span data-stu-id="30153-174">Locating the message download history for a POP3 account</span></span>](locating-the-message-download-history-for-a-pop3-account.md)    
- [<span data-ttu-id="30153-175">POP3 UIDL 履歴の解析</span><span class="sxs-lookup"><span data-stu-id="30153-175">Parsing the POP3 UIDL History</span></span>](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

