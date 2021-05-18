---
title: インデックス作成の MAPI URL Notification-Basedについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422482"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a><span data-ttu-id="1f058-103">インデックス作成の MAPI URL Notification-Basedについて</span><span class="sxs-lookup"><span data-stu-id="1f058-103">About MAPI URLs for Notification-Based Indexing</span></span>

<span data-ttu-id="1f058-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f058-105">ストア プロバイダーは、インデクサーにオブジェクトのインデックス作成の準備ができていることを通知すると、MAPI プロトコル ハンドラーに対してオブジェクトを一意に識別する MAPI URL を生成します。</span><span class="sxs-lookup"><span data-stu-id="1f058-105">When a store provider notifies an indexer that an object is ready for indexing, it generates a MAPI URL that uniquely identifies the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="1f058-106">MAPI URL は Unicode でエンコードされ、次の形式になります。</span><span class="sxs-lookup"><span data-stu-id="1f058-106">MAPI URLs are encoded in Unicode, and have the following format:</span></span> 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

<span data-ttu-id="1f058-107">次の表では、一般的な URL のさまざまな部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="1f058-107">The following table describes the various parts of a typical URL.</span></span>

|<span data-ttu-id="1f058-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="1f058-108">Part</span></span> | <span data-ttu-id="1f058-109">説明</span><span class="sxs-lookup"><span data-stu-id="1f058-109">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="1f058-110">*SID*</span><span class="sxs-lookup"><span data-stu-id="1f058-110">*SID*</span></span> |<span data-ttu-id="1f058-111">現在のユーザーのセキュリティ識別子。</span><span class="sxs-lookup"><span data-stu-id="1f058-111">The current user's security identifier.</span></span>| 
|<span data-ttu-id="1f058-112">*StoreDisplayName*</span><span class="sxs-lookup"><span data-stu-id="1f058-112">*StoreDisplayName*</span></span> |<span data-ttu-id="1f058-113">そのストア上のユーザーの表示名を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="1f058-113">A string that specifies the display name of the user on that store.</span></span>|
|<span data-ttu-id="1f058-114">*HashNumber*</span><span class="sxs-lookup"><span data-stu-id="1f058-114">*HashNumber*</span></span> |<span data-ttu-id="1f058-115">ストア エントリ ID またはストア マッピング署名に基づいて計算される 16 進表記の **DWORD。**</span><span class="sxs-lookup"><span data-stu-id="1f058-115">A **DWORD** in hexadecimal representation that is calculated based on the store entry ID or the store mapping signature.</span></span> <span data-ttu-id="1f058-116">この値はレジストリに格納され、後で MAPI プロトコル ハンドラーのストアを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1f058-116">This value is stored in the registry and will be used later to identify the store in the MAPI Protocol Handler.</span></span><br/><br/><span data-ttu-id="1f058-117">この数値は、他のストアとの競合を最小限に抑える方法で計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f058-117">This number must be calculated in a way that minimizes collisions with other stores.</span></span> <span data-ttu-id="1f058-118">Microsoft がハッシュ番号の計算Outlook使用するアルゴリズムについては[、「Algorithm to Calculate the Store Hash Number」を参照してください](algorithm-to-calculate-the-store-hash-number.md)。</span><span class="sxs-lookup"><span data-stu-id="1f058-118">For the algorithm that Microsoft Outlook uses to calculate the hash number, see [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).</span></span>|
|<span data-ttu-id="1f058-119">*StoreType*</span><span class="sxs-lookup"><span data-stu-id="1f058-119">*StoreType*</span></span> |<span data-ttu-id="1f058-120">インデックスを作成するオブジェクトを含むストアの種類を識別する番号。</span><span class="sxs-lookup"><span data-stu-id="1f058-120">A number that identifies the type of the store that contains the object to be indexed.</span></span> <span data-ttu-id="1f058-121">次の値が示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1f058-121">The possible values are as follows:</span></span><br/><span data-ttu-id="1f058-122">- 0 - 既定のストア。</span><span class="sxs-lookup"><span data-stu-id="1f058-122">- 0 - Default store.</span></span><br/><br/><span data-ttu-id="1f058-123">- 1 - ローカルにキャッシュされたデリゲート アイテムに使用されるデリゲート ストア。</span><span class="sxs-lookup"><span data-stu-id="1f058-123">- 1 - Delegate store, used for delegate items cached locally.</span></span><br/><br/><span data-ttu-id="1f058-124">- 2 - パブリック フォルダー、パブリック フォルダーのお気に入りに使用します。</span><span class="sxs-lookup"><span data-stu-id="1f058-124">- 2 - Public folders, used for public folder favorites.</span></span><br/><br/><span data-ttu-id="1f058-125">**メモ**: ストアがプッシュではなくクロールされている場合、使用される値は文字 *X です*。</span><span class="sxs-lookup"><span data-stu-id="1f058-125">**NOTE**: If the store is being crawled instead of pushed, the value that is used is the character *X*.</span></span>| 
|<span data-ttu-id="1f058-126">*FolderNameA/.../FolderNameN*</span><span class="sxs-lookup"><span data-stu-id="1f058-126">*FolderNameA/…/FolderNameN*</span></span> |<span data-ttu-id="1f058-127">フォルダーのルートからのパスIPM_SUBTREEメッセージに移動します。</span><span class="sxs-lookup"><span data-stu-id="1f058-127">The path from the root of the IPM_SUBTREE to the folder or message.</span></span> <span data-ttu-id="1f058-128">たとえば、[受信トレイ] の [ファミリ] **フォルダー内** の **メッセージには、** この **パラメーターの受信トレイ/ファミリ** があります。</span><span class="sxs-lookup"><span data-stu-id="1f058-128">For example, a message in the **Family** folder under **Inbox** has **Inbox/Family** for this parameter.</span></span> |
|<span data-ttu-id="1f058-129">*EntryIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="1f058-129">*EntryIDEncoded*</span></span> |<span data-ttu-id="1f058-130">Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID。</span><span class="sxs-lookup"><span data-stu-id="1f058-130">MAPI entry ID for the item encoded as a Unicode string.</span></span> <span data-ttu-id="1f058-131">特定の特殊文字のエンコード方法については、以下の「特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f058-131">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="1f058-132">エントリ ID をエンコードするアルゴリズムの詳細については、「Algorithm to Encode Entry IDs and [Attachment ID」を参照してください](algorithm-to-encode-entry-ids-and-attachment-ids.md)。</span><span class="sxs-lookup"><span data-stu-id="1f058-132">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="1f058-133">**メモ**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントに応じて、アルゴリズムに準拠してランダムなハングル文字またはボックスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f058-133">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span>  |
|<span data-ttu-id="1f058-134">*AttachIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="1f058-134">*AttachIDEncoded*</span></span> |<span data-ttu-id="1f058-135">Unicode 文字列としてエンコードされた添付ファイル ID。</span><span class="sxs-lookup"><span data-stu-id="1f058-135">Attachment ID encoded as a Unicode string.</span></span> <span data-ttu-id="1f058-136">特定の特殊文字のエンコード方法については、以下の「特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f058-136">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="1f058-137">エントリ ID をエンコードするアルゴリズムの詳細については、「Algorithm to Encode Entry IDs and [Attachment ID」を参照してください](algorithm-to-encode-entry-ids-and-attachment-ids.md)。</span><span class="sxs-lookup"><span data-stu-id="1f058-137">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="1f058-138">**メモ**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントに応じて、アルゴリズムに準拠してランダムなハングル文字またはボックスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f058-138">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span> |
|<span data-ttu-id="1f058-139">*FileName*</span><span class="sxs-lookup"><span data-stu-id="1f058-139">*FileName*</span></span> |<span data-ttu-id="1f058-140">メッセージに表示される添付ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="1f058-140">Name of the attachment file, as it appears in the message.</span></span>|
    
## <a name="examples-of-mapi-urls"></a><span data-ttu-id="1f058-141">MAPI URL の例</span><span class="sxs-lookup"><span data-stu-id="1f058-141">Examples of MAPI URLs</span></span>

<span data-ttu-id="1f058-142">MAPI URL の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1f058-142">The following are some examples of MAPI URLs.</span></span>
  
- <span data-ttu-id="1f058-143">フォルダーの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="1f058-143">MAPI URL for a folder:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- <span data-ttu-id="1f058-144">メッセージの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="1f058-144">MAPI URL for a message:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- <span data-ttu-id="1f058-145">添付ファイルの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="1f058-145">MAPI URL for an attachment:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a><span data-ttu-id="1f058-146">特殊文字</span><span class="sxs-lookup"><span data-stu-id="1f058-146">Special characters</span></span>

<span data-ttu-id="1f058-147">メッセージまたは添付ファイルに表示される場合、特定の文字がエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="1f058-147">Certain characters are encoded if they appear in the message or attachment.</span></span> <span data-ttu-id="1f058-148">MAPI URL でエンコードされる文字を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1f058-148">The following shows which characters are encoded in a MAPI URL:</span></span>
  
- <span data-ttu-id="1f058-149">% > %25</span><span class="sxs-lookup"><span data-stu-id="1f058-149">% > %25</span></span>
    
- <span data-ttu-id="1f058-150">/ > %2F</span><span class="sxs-lookup"><span data-stu-id="1f058-150">/ > %2F</span></span> 
    
- <span data-ttu-id="1f058-151">\ > %5C</span><span class="sxs-lookup"><span data-stu-id="1f058-151">\ > %5C</span></span> 
    
- <span data-ttu-id="1f058-152">\* > %2A</span><span class="sxs-lookup"><span data-stu-id="1f058-152">\* > %2A</span></span> 
    
- <span data-ttu-id="1f058-153">?</span><span class="sxs-lookup"><span data-stu-id="1f058-153">?</span></span> <span data-ttu-id="1f058-154">> %3F</span><span class="sxs-lookup"><span data-stu-id="1f058-154">> %3F</span></span> 
    
## <a name="blob-associated-with-each-mapi-url"></a><span data-ttu-id="1f058-155">各 MAPI URL に関連付けられた BLOB</span><span class="sxs-lookup"><span data-stu-id="1f058-155">Blob associated with each MAPI URL</span></span>

<span data-ttu-id="1f058-156">インデックスを作成するオブジェクトの MAPI URL をプッシュすると、ストア プロバイダーは MAPI プロトコル ハンドラーの特定の情報を含むバイナリ ラージ オブジェクト (BLOB) も作成します。</span><span class="sxs-lookup"><span data-stu-id="1f058-156">When pushing a MAPI URL for an object to be indexed, a store provider also creates a binary large object (BLOB) that contains certain information for the MAPI Protocol Handler.</span></span> <span data-ttu-id="1f058-157">ストア プロバイダーは、この BLOB を各 MAPI URL に関連付け、MAPI URL をインデクサーにプッシュするときに送信します。</span><span class="sxs-lookup"><span data-stu-id="1f058-157">The store provider associates this BLOB with each MAPI URL and sends it when pushing the MAPI URL to the indexer.</span></span> <span data-ttu-id="1f058-158">BLOB の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1f058-158">The format of the BLOB is as follows:</span></span> 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

<span data-ttu-id="1f058-159">ストア プロバイダーは、これらの値を示す順序で BLOB に書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f058-159">The store provider must write these values to the BLOB in the order shown.</span></span> <span data-ttu-id="1f058-160">次の表では、BLOB の各フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1f058-160">The following table describes each field of the BLOB.</span></span>

|<span data-ttu-id="1f058-161">指定項目</span><span class="sxs-lookup"><span data-stu-id="1f058-161">Part</span></span> | <span data-ttu-id="1f058-162">説明</span><span class="sxs-lookup"><span data-stu-id="1f058-162">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="1f058-163">*dwVersion*</span><span class="sxs-lookup"><span data-stu-id="1f058-163">*dwVersion*</span></span> |<span data-ttu-id="1f058-164">これは、送信されるデータのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="1f058-164">This is the version of the data being sent.</span></span> <span data-ttu-id="1f058-165">現在、この値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="1f058-165">Currently this value is 1.</span></span>|
|<span data-ttu-id="1f058-166">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1f058-166">*dwFlags*</span></span> |<span data-ttu-id="1f058-167">将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="1f058-167">Reserved for future use.</span></span> <span data-ttu-id="1f058-168">現在、この値は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f058-168">Currently this value should be 0.</span></span>|
|<span data-ttu-id="1f058-169">*cbProfileName*</span><span class="sxs-lookup"><span data-stu-id="1f058-169">*cbProfileName*</span></span> |<span data-ttu-id="1f058-170">プロファイル名のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="1f058-170">The size of the profile name, in bytes.</span></span> <span data-ttu-id="1f058-171">この情報は、MAPI プロトコル ハンドラーがアイテムのインデックス作成時に使用するプロファイルを知る際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1f058-171">This information is useful for the MAPI Protocol Handler to know which profile to use when indexing the item.</span></span>|
|<span data-ttu-id="1f058-172">*wszProfileName*</span><span class="sxs-lookup"><span data-stu-id="1f058-172">*wszProfileName*</span></span> |<span data-ttu-id="1f058-173">プロファイル名を含む Null 終端 Unicode 文字列。</span><span class="sxs-lookup"><span data-stu-id="1f058-173">Null-terminated Unicode string that contains the profile name.</span></span>|
|<span data-ttu-id="1f058-174">*cbProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="1f058-174">*cbProviderItemID*</span></span> |<span data-ttu-id="1f058-175">プロバイダー アイテム ID のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="1f058-175">Size of the provider item ID, in bytes.</span></span> <span data-ttu-id="1f058-176">ストア プロバイダーは、この情報を取得するために追加のフォルダーを開かねないで、フォルダーのプロバイダー アイテム ID のみを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f058-176">The store provider should send only the provider item ID for folders, to prevent opening additional folders to get this information.</span></span>|
|<span data-ttu-id="1f058-177">*wszProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="1f058-177">*wszProviderItemID*</span></span> |<span data-ttu-id="1f058-178">ストア内のアイテムを一意に識別するプロバイダー アイテム ID を持つ Null で終了する Unicode 文字列。</span><span class="sxs-lookup"><span data-stu-id="1f058-178">Null-terminated Unicode string with the provider item ID that uniquely identifies the item in the store.</span></span>|
    
## <a name="see-also"></a><span data-ttu-id="1f058-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f058-179">See also</span></span>

- [<span data-ttu-id="1f058-180">ストア インデックスNotification-Basedについて</span><span class="sxs-lookup"><span data-stu-id="1f058-180">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="1f058-181">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="1f058-181">MAPI Constants</span></span>](mapi-constants.md)

