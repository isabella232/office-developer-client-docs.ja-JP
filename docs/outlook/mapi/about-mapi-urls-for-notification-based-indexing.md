---
title: 通知ベースのインデックス作成の MAPI URL について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 57868996f95cfb135298378d2638bc57b2e69977
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583674"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a><span data-ttu-id="e1a6e-103">通知ベースのインデックス作成の MAPI URL について</span><span class="sxs-lookup"><span data-stu-id="e1a6e-103">About MAPI URLs for Notification-Based Indexing</span></span>

<span data-ttu-id="e1a6e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1a6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1a6e-105">ストア プロバイダーには、オブジェクトのインデックス作成の準備が整っているインデクサーが通知された、MAPI プロトコル ハンドラー オブジェクトを一意に識別する MAPI URL が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-105">When a store provider notifies an indexer that an object is ready for indexing, it generates a MAPI URL that uniquely identifies the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="e1a6e-106">MAPI Url、Unicode でエンコードされた、次の形式。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-106">MAPI URLs are encoded in Unicode, and have the following format:</span></span> 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

<span data-ttu-id="e1a6e-107">次の表では、一般的な URL の各部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-107">The following table describes the various parts of a typical URL.</span></span>

|<span data-ttu-id="e1a6e-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="e1a6e-108">Part</span></span> | <span data-ttu-id="e1a6e-109">説明</span><span class="sxs-lookup"><span data-stu-id="e1a6e-109">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="e1a6e-110">*SID*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-110">*SID*</span></span> |<span data-ttu-id="e1a6e-111">現在のユーザーのセキュリティ識別子です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-111">The current user's security identifier.</span></span>| 
|<span data-ttu-id="e1a6e-112">*StoreDisplayName*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-112">*StoreDisplayName*</span></span> |<span data-ttu-id="e1a6e-113">そのストア上で、ユーザーの表示名を指定する文字列です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-113">A string that specifies the display name of the user on that store.</span></span>|
|<span data-ttu-id="e1a6e-114">*ハッシュ番号*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-114">*HashNumber*</span></span> |<span data-ttu-id="e1a6e-115">計算された 16 進数表現では、 **DWORD**は、ストア エントリ ID またはストア マッピングの署名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-115">A **DWORD** in hexadecimal representation that is calculated based on the store entry ID or the store mapping signature.</span></span> <span data-ttu-id="e1a6e-116">この値は、レジストリに格納されているが、MAPI プロトコル ハンドラーでストアを識別するのには後で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-116">This value is stored in the registry and will be used later to identify the store in the MAPI Protocol Handler.</span></span><br/><br/><span data-ttu-id="e1a6e-117">この数値は、他のストアとの衝突を最小限に抑える方法で計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-117">This number must be calculated in a way that minimizes collisions with other stores.</span></span> <span data-ttu-id="e1a6e-118">Microsoft Outlook を使用してハッシュを計算するアルゴリズムでは、[番号を保存するハッシュを計算するアルゴリズム](algorithm-to-calculate-the-store-hash-number.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-118">For the algorithm that Microsoft Outlook uses to calculate the hash number, see [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).</span></span>|
|<span data-ttu-id="e1a6e-119">*StoreType*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-119">*StoreType*</span></span> |<span data-ttu-id="e1a6e-120">インデックスを作成するオブジェクトが含まれるストアの種類を識別する番号です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-120">A number that identifies the type of the store that contains the object to be indexed.</span></span> <span data-ttu-id="e1a6e-121">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-121">The possible values are as follows:</span></span><br/><span data-ttu-id="e1a6e-122">-0 - 既定のストアです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-122">- 0 - Default store.</span></span><br/><br/><span data-ttu-id="e1a6e-123">-代理ストアを 1 -、代理人のアイテムがローカルにキャッシュを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-123">- 1 - Delegate store, used for delegate items cached locally.</span></span><br/><br/><span data-ttu-id="e1a6e-124">-2 - パブリック フォルダー、パブリック フォルダーのお気に入りを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-124">- 2 - Public folders, used for public folder favorites.</span></span><br/><br/><span data-ttu-id="e1a6e-125">**注**: ストアは、プッシュの代わりにクロールするが、使用される値が*X*の文字です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-125">**NOTE**: If the store is being crawled instead of pushed, the value that is used is the character*X*.</span></span>| 
|<span data-ttu-id="e1a6e-126">*FolderNameA/.../FolderNameN*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-126">*FolderNameA/…/FolderNameN*</span></span> |<span data-ttu-id="e1a6e-127">IPM_SUBTREE のルートからフォルダーまたはメッセージへのパスです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-127">The path from the root of the IPM_SUBTREE to the folder or message.</span></span> <span data-ttu-id="e1a6e-128">たとえば、 **[受信トレイ]** の下で [**ファミリ**] フォルダーにメッセージは、このパラメーターの**受信トレイと家族**を持っています。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-128">For example, a message in the **Family** folder under **Inbox** has **Inbox/Family** for this parameter.</span></span> |
|<span data-ttu-id="e1a6e-129">*EntryIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-129">*EntryIDEncoded*</span></span> |<span data-ttu-id="e1a6e-130">Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-130">MAPI entry ID for the item encoded as a Unicode string.</span></span> <span data-ttu-id="e1a6e-131">特定の特殊文字をエンコードする方法については、次のセクション特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-131">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="e1a6e-132">エントリ ID をエンコードするためのアルゴリズムの詳細については、[アルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-132">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="e1a6e-133">**注**: ランダムのハングル文字または使用可能なフォントに応じて、アルゴリズムに準拠しているボックスに ID が表示されるエントリがこのエンコードされたテキストとして表示するときです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-133">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span>  |
|<span data-ttu-id="e1a6e-134">*AttachIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-134">*AttachIDEncoded*</span></span> |<span data-ttu-id="e1a6e-135">Unicode 文字列としてエンコードされた添付ファイルの ID です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-135">Attachment ID encoded as a Unicode string.</span></span> <span data-ttu-id="e1a6e-136">特定の特殊文字をエンコードする方法については、次のセクション特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-136">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="e1a6e-137">エントリ ID をエンコードするためのアルゴリズムの詳細については、[アルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-137">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="e1a6e-138">**注**: ランダムのハングル文字または使用可能なフォントに応じて、アルゴリズムに準拠しているボックスに ID が表示されるエントリがこのエンコードされたテキストとして表示するときです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-138">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span> |
|<span data-ttu-id="e1a6e-139">*Filename*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-139">*FileName*</span></span> |<span data-ttu-id="e1a6e-140">添付ファイルの名前、メッセージに表示されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-140">Name of the attachment file, as it appears in the message.</span></span>|
    
## <a name="examples-of-mapi-urls"></a><span data-ttu-id="e1a6e-141">MAPI Url の例</span><span class="sxs-lookup"><span data-stu-id="e1a6e-141">Examples of MAPI URLs</span></span>

<span data-ttu-id="e1a6e-142">MAPI Url の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-142">The following are some examples of MAPI URLs.</span></span>
  
- <span data-ttu-id="e1a6e-143">フォルダーの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="e1a6e-143">MAPI URL for a folder:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- <span data-ttu-id="e1a6e-144">メッセージの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="e1a6e-144">MAPI URL for a message:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- <span data-ttu-id="e1a6e-145">添付ファイルは MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="e1a6e-145">MAPI URL for an attachment:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a><span data-ttu-id="e1a6e-146">特殊文字</span><span class="sxs-lookup"><span data-stu-id="e1a6e-146">Special characters</span></span>

<span data-ttu-id="e1a6e-147">メッセージまたは添付ファイルに含まれる場合は、特定の文字がエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-147">Certain characters are encoded if they appear in the message or attachment.</span></span> <span data-ttu-id="e1a6e-148">MAPI URL をエンコードする文字を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-148">The following shows which characters are encoded in a MAPI URL:</span></span>
  
- <span data-ttu-id="e1a6e-149">% > %25</span><span class="sxs-lookup"><span data-stu-id="e1a6e-149">% > %25</span></span>
    
- <span data-ttu-id="e1a6e-150">/> %2f</span><span class="sxs-lookup"><span data-stu-id="e1a6e-150">/ > %2F</span></span> 
    
- <span data-ttu-id="e1a6e-151">\ > %5 C</span><span class="sxs-lookup"><span data-stu-id="e1a6e-151">\ > %5C</span></span> 
    
- <span data-ttu-id="e1a6e-152">\*> %2a</span><span class="sxs-lookup"><span data-stu-id="e1a6e-152">\* > %2A</span></span> 
    
- <span data-ttu-id="e1a6e-153">?</span><span class="sxs-lookup"><span data-stu-id="e1a6e-153"></span></span> <span data-ttu-id="e1a6e-154">> %3f</span><span class="sxs-lookup"><span data-stu-id="e1a6e-154">> %3F</span></span> 
    
## <a name="blob-associated-with-each-mapi-url"></a><span data-ttu-id="e1a6e-155">各 MAPI URL に関連付けられた blob</span><span class="sxs-lookup"><span data-stu-id="e1a6e-155">Blob associated with each MAPI URL</span></span>

<span data-ttu-id="e1a6e-156">オブジェクトのインデックスを作成する MAPI URL をプッシュするには、ストア プロバイダーは、MAPI プロトコル ハンドラーの特定の情報を格納するバイナリ ラージ オブジェクト (BLOB) をも作成します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-156">When pushing a MAPI URL for an object to be indexed, a store provider also creates a binary large object (BLOB) that contains certain information for the MAPI Protocol Handler.</span></span> <span data-ttu-id="e1a6e-157">ストア プロバイダーは、各 MAPI URL を使用してこの BLOB に関連付けるし、MAPI URL がインデクサーにプッシュするときに送信します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-157">The store provider associates this BLOB with each MAPI URL and sends it when pushing the MAPI URL to the indexer.</span></span> <span data-ttu-id="e1a6e-158">BLOB の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-158">The format of the BLOB is as follows:</span></span> 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

<span data-ttu-id="e1a6e-159">ストア プロバイダーは、以下の順に BLOB をこれらの値を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-159">The store provider must write these values to the BLOB in the order shown.</span></span> <span data-ttu-id="e1a6e-160">次の表では、BLOB の各フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-160">The following table describes each field of the BLOB.</span></span>

|<span data-ttu-id="e1a6e-161">パーツ</span><span class="sxs-lookup"><span data-stu-id="e1a6e-161">Part</span></span> | <span data-ttu-id="e1a6e-162">説明</span><span class="sxs-lookup"><span data-stu-id="e1a6e-162">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="e1a6e-163">*dwVersion*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-163">*dwVersion*</span></span> |<span data-ttu-id="e1a6e-164">これは、送信されるデータのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-164">This is the version of the data being sent.</span></span> <span data-ttu-id="e1a6e-165">現在、この値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-165">Currently this value is 1.</span></span>|
|<span data-ttu-id="e1a6e-166">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-166">*dwFlags*</span></span> |<span data-ttu-id="e1a6e-167">将来の使用のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-167">Reserved for future use.</span></span> <span data-ttu-id="e1a6e-168">現在この値は 0 を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-168">Currently this value should be 0.</span></span>|
|<span data-ttu-id="e1a6e-169">*cbProfileName*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-169">*cbProfileName*</span></span> |<span data-ttu-id="e1a6e-170">バイトで、プロファイル名のサイズです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-170">The size of the profile name, in bytes.</span></span> <span data-ttu-id="e1a6e-171">この情報は、MAPI プロトコル ハンドラーは、項目のインデックスを作成するときに使用するプロファイルを知っている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-171">This information is useful for the MAPI Protocol Handler to know which profile to use when indexing the item.</span></span>|
|<span data-ttu-id="e1a6e-172">*wszProfileName*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-172">*wszProfileName*</span></span> |<span data-ttu-id="e1a6e-173">Null で終わる Unicode 文字列プロファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-173">Null-terminated Unicode string that contains the profile name.</span></span>|
|<span data-ttu-id="e1a6e-174">*cbProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-174">*cbProviderItemID*</span></span> |<span data-ttu-id="e1a6e-175">プロバイダー アイテム ID のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-175">Size of the provider item ID, in bytes.</span></span> <span data-ttu-id="e1a6e-176">ストア プロバイダーは、この情報を取得する追加のフォルダーを開けないようにするのには、フォルダーのアイテムの ID プロバイダーのみを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-176">The store provider should send only the provider item ID for folders, to prevent opening additional folders to get this information.</span></span>|
|<span data-ttu-id="e1a6e-177">*wszProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="e1a6e-177">*wszProviderItemID*</span></span> |<span data-ttu-id="e1a6e-178">Null で終わる Unicode 文字列ストア内の項目を一意に識別するプロバイダー アイテム ID を持つ。</span><span class="sxs-lookup"><span data-stu-id="e1a6e-178">Null-terminated Unicode string with the provider item ID that uniquely identifies the item in the store.</span></span>|
    
## <a name="see-also"></a><span data-ttu-id="e1a6e-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1a6e-179">See also</span></span>

- [<span data-ttu-id="e1a6e-180">通知ベースのストア インデックス作成について</span><span class="sxs-lookup"><span data-stu-id="e1a6e-180">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="e1a6e-181">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="e1a6e-181">MAPI Constants</span></span>](mapi-constants.md)

