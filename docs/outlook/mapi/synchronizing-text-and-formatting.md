---
title: テキストと書式設定を同期する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346600"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="5b9b3-103">テキストと書式設定を同期する</span><span class="sxs-lookup"><span data-stu-id="5b9b3-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="5b9b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b9b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b9b3-105">リッチテキスト形式 (RTF) メッセージを送信する際の主な課題は、テキストを書式設定と同期させることです。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="5b9b3-106">メッセージが宛先に到着したときに、メッセージが発信者として送信され、テキストと書式設定が同期されるようにするために、MAPI は[rtfsync](rtfsync.md)関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="5b9b3-107">**rtfsync**は、通常、受信メッセージを表示する前に RTF 対応クライアントによって呼び出され、トランスポートプロバイダーにメッセージをダウンロードするときに MAPI スプーラーを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="5b9b3-108">発信者は、1つまたは2つのフラグを**rtfsync**に渡すことによって、起こり得る不一致の領域を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="5b9b3-109">RTF_SYNC_BODY_CHANGED は、メッセージテキストの変更を示します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="5b9b3-110">RTF_SYNC_RTF_CHANGED は、メッセージ形式の変更を示します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="5b9b3-111">**rtfsync**で行われる同期プロセスは、一部の文字を無視して他を変換する、メッセージテキストの高度な巡回冗長チェック (CRC) です。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="5b9b3-112">トランスポートプロバイダーによって追加された可能性のある文字は無視されます。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="5b9b3-113">MAPI では、次の表に示すように、RTF を処理するためのいくつかのプロパティが定義されています。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="5b9b3-114">**RTF プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5b9b3-114">**RTF property**</span></span>|<span data-ttu-id="5b9b3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b9b3-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b9b3-116">**PR_RTF_SYNC_BODY_TAG**([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b9b3-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b9b3-117">実際のメッセージテキストの先頭を示します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="5b9b3-118">**PR_RTF_SYNC_BODY_CRC**([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b9b3-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b9b3-119">メッセージテキストの巡回冗長チェックの結果を格納します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="5b9b3-120">**PR_RTF_SYNC_BODY_COUNT**([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b9b3-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b9b3-121">**PR_RTF_SYNC_BODY_CRC**の文字数を含みます。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="5b9b3-122">**PR_RTF_IN_SYNC**([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b9b3-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b9b3-123">メッセージテキストと書式設定が同期されている場合は TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="5b9b3-124">**PR_RTF_SYNC_PREFIX_COUNT**([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b9b3-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b9b3-125">メッセージテキストを preceed する空白以外の文字の数を含みます。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="5b9b3-126">**PR_RTF_SYNC_TRAILING_COUNT**([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b9b3-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b9b3-127">メッセージテキストを記録する空白以外の文字の数を含みます。</span><span class="sxs-lookup"><span data-stu-id="5b9b3-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

