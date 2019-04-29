---
title: 通知ベースのインデックス作成の MAPI url について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422482"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a><span data-ttu-id="8a710-103">通知ベースのインデックス作成の MAPI url について</span><span class="sxs-lookup"><span data-stu-id="8a710-103">About MAPI URLs for Notification-Based Indexing</span></span>

<span data-ttu-id="8a710-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a710-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a710-105">ストアプロバイダーは、オブジェクトがインデックス処理の準備が整っていることをインデクサーに通知すると、mapi プロトコルハンドラーにオブジェクトを一意に識別する mapi URL を生成します。</span><span class="sxs-lookup"><span data-stu-id="8a710-105">When a store provider notifies an indexer that an object is ready for indexing, it generates a MAPI URL that uniquely identifies the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="8a710-106">MAPI url は Unicode でエンコードされ、次の形式になります。</span><span class="sxs-lookup"><span data-stu-id="8a710-106">MAPI URLs are encoded in Unicode, and have the following format:</span></span> 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

<span data-ttu-id="8a710-107">次の表に、一般的な URL のさまざまな部分を示します。</span><span class="sxs-lookup"><span data-stu-id="8a710-107">The following table describes the various parts of a typical URL.</span></span>

|<span data-ttu-id="8a710-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="8a710-108">Part</span></span> | <span data-ttu-id="8a710-109">説明</span><span class="sxs-lookup"><span data-stu-id="8a710-109">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="8a710-110">*SID*</span><span class="sxs-lookup"><span data-stu-id="8a710-110">*SID*</span></span> |<span data-ttu-id="8a710-111">現在のユーザーのセキュリティ識別子。</span><span class="sxs-lookup"><span data-stu-id="8a710-111">The current user's security identifier.</span></span>| 
|<span data-ttu-id="8a710-112">*storedisplayname*</span><span class="sxs-lookup"><span data-stu-id="8a710-112">*StoreDisplayName*</span></span> |<span data-ttu-id="8a710-113">そのストア上のユーザーの表示名を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8a710-113">A string that specifies the display name of the user on that store.</span></span>|
|<span data-ttu-id="8a710-114">*hashnumber*</span><span class="sxs-lookup"><span data-stu-id="8a710-114">*HashNumber*</span></span> |<span data-ttu-id="8a710-115">ストアエントリ ID またはストアマッピングシグネチャに基づいて計算される16進表記の**DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="8a710-115">A **DWORD** in hexadecimal representation that is calculated based on the store entry ID or the store mapping signature.</span></span> <span data-ttu-id="8a710-116">この値は、レジストリに格納され、後で MAPI プロトコルハンドラーでストアを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a710-116">This value is stored in the registry and will be used later to identify the store in the MAPI Protocol Handler.</span></span><br/><br/><span data-ttu-id="8a710-117">この数値は、他のストアとの競合を最小限に抑えるように計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a710-117">This number must be calculated in a way that minimizes collisions with other stores.</span></span> <span data-ttu-id="8a710-118">Microsoft Outlook がハッシュ番号を計算するために使用するアルゴリズムについては、「 [Store ハッシュ番号を計算するアルゴリズム](algorithm-to-calculate-the-store-hash-number.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a710-118">For the algorithm that Microsoft Outlook uses to calculate the hash number, see [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).</span></span>|
|<span data-ttu-id="8a710-119">*StoreType*</span><span class="sxs-lookup"><span data-stu-id="8a710-119">*StoreType*</span></span> |<span data-ttu-id="8a710-120">インデックスを作成するオブジェクトが格納されているストアの種類を識別する番号。</span><span class="sxs-lookup"><span data-stu-id="8a710-120">A number that identifies the type of the store that contains the object to be indexed.</span></span> <span data-ttu-id="8a710-121">次の値が示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8a710-121">The possible values are as follows:</span></span><br/><span data-ttu-id="8a710-122">-0-既定のストア。</span><span class="sxs-lookup"><span data-stu-id="8a710-122">- 0 - Default store.</span></span><br/><br/><span data-ttu-id="8a710-123">-1-ローカルにキャッシュされた代理人のアイテムに使用される代理人ストア。</span><span class="sxs-lookup"><span data-stu-id="8a710-123">- 1 - Delegate store, used for delegate items cached locally.</span></span><br/><br/><span data-ttu-id="8a710-124">-2-パブリックフォルダーのお気に入りに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a710-124">- 2 - Public folders, used for public folder favorites.</span></span><br/><br/><span data-ttu-id="8a710-125">**注**: ストアがプッシュされる代わりにクロールされる場合、使用される値は文字*X*です。</span><span class="sxs-lookup"><span data-stu-id="8a710-125">**NOTE**: If the store is being crawled instead of pushed, the value that is used is the character*X*.</span></span>| 
|<span data-ttu-id="8a710-126">*foldernamea/.../foldernamea*</span><span class="sxs-lookup"><span data-stu-id="8a710-126">*FolderNameA/…/FolderNameN*</span></span> |<span data-ttu-id="8a710-127">フォルダーまたはメッセージへの IPM_SUBTREE のルートからのパス。</span><span class="sxs-lookup"><span data-stu-id="8a710-127">The path from the root of the IPM_SUBTREE to the folder or message.</span></span> <span data-ttu-id="8a710-128">たとえば、**受信トレイ**の下にある [**家族**] フォルダー内のメッセージには、このパラメーターの**inbox/Family**があります。</span><span class="sxs-lookup"><span data-stu-id="8a710-128">For example, a message in the **Family** folder under **Inbox** has **Inbox/Family** for this parameter.</span></span> |
|<span data-ttu-id="8a710-129">*entryidencoded*</span><span class="sxs-lookup"><span data-stu-id="8a710-129">*EntryIDEncoded*</span></span> |<span data-ttu-id="8a710-130">Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID。</span><span class="sxs-lookup"><span data-stu-id="8a710-130">MAPI entry ID for the item encoded as a Unicode string.</span></span> <span data-ttu-id="8a710-131">特定の特殊文字がどのようにエンコードされるかについては、以下の「特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a710-131">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="8a710-132">エントリ id をエンコードするアルゴリズムの詳細については、「 [entry id とアタッチメント id をエンコードするためのアルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a710-132">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="8a710-133">**注**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントによっては、アルゴリズムに準拠して、ハングル文字またはボックスがランダムに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a710-133">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span>  |
|<span data-ttu-id="8a710-134">*attachidencoded*</span><span class="sxs-lookup"><span data-stu-id="8a710-134">*AttachIDEncoded*</span></span> |<span data-ttu-id="8a710-135">Unicode 文字列としてエンコードされた添付ファイル ID。</span><span class="sxs-lookup"><span data-stu-id="8a710-135">Attachment ID encoded as a Unicode string.</span></span> <span data-ttu-id="8a710-136">特定の特殊文字がどのようにエンコードされるかについては、以下の「特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a710-136">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="8a710-137">エントリ id をエンコードするアルゴリズムの詳細については、「 [entry id とアタッチメント id をエンコードするためのアルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a710-137">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="8a710-138">**注**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントによっては、アルゴリズムに準拠して、ハングル文字またはボックスがランダムに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a710-138">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span> |
|<span data-ttu-id="8a710-139">*FileName*</span><span class="sxs-lookup"><span data-stu-id="8a710-139">*FileName*</span></span> |<span data-ttu-id="8a710-140">添付ファイルの名前。メッセージに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a710-140">Name of the attachment file, as it appears in the message.</span></span>|
    
## <a name="examples-of-mapi-urls"></a><span data-ttu-id="8a710-141">MAPI url の例</span><span class="sxs-lookup"><span data-stu-id="8a710-141">Examples of MAPI URLs</span></span>

<span data-ttu-id="8a710-142">次に、MAPI url の例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="8a710-142">The following are some examples of MAPI URLs.</span></span>
  
- <span data-ttu-id="8a710-143">フォルダーの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="8a710-143">MAPI URL for a folder:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- <span data-ttu-id="8a710-144">メッセージの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="8a710-144">MAPI URL for a message:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- <span data-ttu-id="8a710-145">添付ファイルの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="8a710-145">MAPI URL for an attachment:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a><span data-ttu-id="8a710-146">特殊文字</span><span class="sxs-lookup"><span data-stu-id="8a710-146">Special characters</span></span>

<span data-ttu-id="8a710-147">メッセージまたは添付ファイルに表示されている場合、特定の文字はエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="8a710-147">Certain characters are encoded if they appear in the message or attachment.</span></span> <span data-ttu-id="8a710-148">次に、MAPI URL でエンコードされる文字を示します。</span><span class="sxs-lookup"><span data-stu-id="8a710-148">The following shows which characters are encoded in a MAPI URL:</span></span>
  
- <span data-ttu-id="8a710-149">% >% 25</span><span class="sxs-lookup"><span data-stu-id="8a710-149">% > %25</span></span>
    
- <span data-ttu-id="8a710-150">/>% 2f</span><span class="sxs-lookup"><span data-stu-id="8a710-150">/ > %2F</span></span> 
    
- <span data-ttu-id="8a710-151">\ >% 5c</span><span class="sxs-lookup"><span data-stu-id="8a710-151">\ > %5C</span></span> 
    
- <span data-ttu-id="8a710-152">\*>% 2a</span><span class="sxs-lookup"><span data-stu-id="8a710-152">\* > %2A</span></span> 
    
- <span data-ttu-id="8a710-153">?</span><span class="sxs-lookup"><span data-stu-id="8a710-153"></span></span> <span data-ttu-id="8a710-154">>% 3f</span><span class="sxs-lookup"><span data-stu-id="8a710-154">> %3F</span></span> 
    
## <a name="blob-associated-with-each-mapi-url"></a><span data-ttu-id="8a710-155">各 MAPI URL に関連付けられている Blob</span><span class="sxs-lookup"><span data-stu-id="8a710-155">Blob associated with each MAPI URL</span></span>

<span data-ttu-id="8a710-156">インデックスを作成するオブジェクトの mapi URL をプッシュするときに、ストアプロバイダーは、mapi プロトコルハンドラーの特定の情報を含むバイナリラージオブジェクト (BLOB) も作成します。</span><span class="sxs-lookup"><span data-stu-id="8a710-156">When pushing a MAPI URL for an object to be indexed, a store provider also creates a binary large object (BLOB) that contains certain information for the MAPI Protocol Handler.</span></span> <span data-ttu-id="8a710-157">ストアプロバイダーは、この BLOB を各 mapi url に関連付け、mapi url をインデクサーにプッシュするときに送信します。</span><span class="sxs-lookup"><span data-stu-id="8a710-157">The store provider associates this BLOB with each MAPI URL and sends it when pushing the MAPI URL to the indexer.</span></span> <span data-ttu-id="8a710-158">BLOB の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8a710-158">The format of the BLOB is as follows:</span></span> 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

<span data-ttu-id="8a710-159">ストアプロバイダーは、表示されている順序でこれらの値を BLOB に書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a710-159">The store provider must write these values to the BLOB in the order shown.</span></span> <span data-ttu-id="8a710-160">次の表では、BLOB の各フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8a710-160">The following table describes each field of the BLOB.</span></span>

|<span data-ttu-id="8a710-161">パーツ</span><span class="sxs-lookup"><span data-stu-id="8a710-161">Part</span></span> | <span data-ttu-id="8a710-162">説明</span><span class="sxs-lookup"><span data-stu-id="8a710-162">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="8a710-163">*dwversion*</span><span class="sxs-lookup"><span data-stu-id="8a710-163">*dwVersion*</span></span> |<span data-ttu-id="8a710-164">これは、送信されるデータのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="8a710-164">This is the version of the data being sent.</span></span> <span data-ttu-id="8a710-165">現在、この値は1です。</span><span class="sxs-lookup"><span data-stu-id="8a710-165">Currently this value is 1.</span></span>|
|<span data-ttu-id="8a710-166">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8a710-166">*dwFlags*</span></span> |<span data-ttu-id="8a710-167">将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="8a710-167">Reserved for future use.</span></span> <span data-ttu-id="8a710-168">現在、この値は0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a710-168">Currently this value should be 0.</span></span>|
|<span data-ttu-id="8a710-169">*cbprofilename*</span><span class="sxs-lookup"><span data-stu-id="8a710-169">*cbProfileName*</span></span> |<span data-ttu-id="8a710-170">プロファイル名のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="8a710-170">The size of the profile name, in bytes.</span></span> <span data-ttu-id="8a710-171">この情報は、MAPI プロトコルハンドラーがアイテムのインデックス作成時に使用するプロファイルを知るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8a710-171">This information is useful for the MAPI Protocol Handler to know which profile to use when indexing the item.</span></span>|
|<span data-ttu-id="8a710-172">*wszProfileName*</span><span class="sxs-lookup"><span data-stu-id="8a710-172">*wszProfileName*</span></span> |<span data-ttu-id="8a710-173">プロファイル名を含む Null で終わる Unicode 文字列。</span><span class="sxs-lookup"><span data-stu-id="8a710-173">Null-terminated Unicode string that contains the profile name.</span></span>|
|<span data-ttu-id="8a710-174">*cbprovideritemid*</span><span class="sxs-lookup"><span data-stu-id="8a710-174">*cbProviderItemID*</span></span> |<span data-ttu-id="8a710-175">プロバイダーアイテム ID のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="8a710-175">Size of the provider item ID, in bytes.</span></span> <span data-ttu-id="8a710-176">ストアプロバイダーは、フォルダーのプロバイダアイテム ID のみを送信して、この情報を取得するために追加のフォルダーを開かないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a710-176">The store provider should send only the provider item ID for folders, to prevent opening additional folders to get this information.</span></span>|
|<span data-ttu-id="8a710-177">*wszProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="8a710-177">*wszProviderItemID*</span></span> |<span data-ttu-id="8a710-178">ストア内のアイテムを一意に識別するプロバイダアイテム ID を持つ、Null で終了する Unicode 文字列。</span><span class="sxs-lookup"><span data-stu-id="8a710-178">Null-terminated Unicode string with the provider item ID that uniquely identifies the item in the store.</span></span>|
    
## <a name="see-also"></a><span data-ttu-id="8a710-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a710-179">See also</span></span>

- [<span data-ttu-id="8a710-180">通知ベースのストアインデックス作成について</span><span class="sxs-lookup"><span data-stu-id="8a710-180">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="8a710-181">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="8a710-181">MAPI Constants</span></span>](mapi-constants.md)

