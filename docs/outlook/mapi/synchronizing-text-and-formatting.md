---
title: テキストと書式設定の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435104"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="21228-103">テキストと書式設定の同期</span><span class="sxs-lookup"><span data-stu-id="21228-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="21228-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21228-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21228-105">リッチ テキスト形式 (RTF) メッセージを送信する主な課題は、テキストと書式設定の同期を維持することです。</span><span class="sxs-lookup"><span data-stu-id="21228-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="21228-106">メッセージが宛先に到着すると、その発信元が意図した通りであり、テキストと書式設定が同期することを確認するために、MAPI は [RTFSync 関数を提供](rtfsync.md) します。</span><span class="sxs-lookup"><span data-stu-id="21228-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="21228-107">**RTFSync** は通常、受信メッセージを表示する前に RTF 対応クライアントによって呼び出され、トランスポート プロバイダーにメッセージをダウンロードするときに MAPI スプーラーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="21228-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="21228-108">呼び出し元は、RTFSync に 1 つまたは 2 つのフラグを渡して、可能な不一致の領域 **を指定します**。</span><span class="sxs-lookup"><span data-stu-id="21228-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="21228-109">RTF_SYNC_BODY_CHANGEDテキストの変更を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="21228-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="21228-110">RTF_SYNC_RTF_CHANGED書式の変更を示す場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="21228-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="21228-111">**RTFSync** で発生する同期プロセスは、一部の文字を無視して他の文字を変換するメッセージ テキストの高度な循環冗長チェック (CRC) です。</span><span class="sxs-lookup"><span data-stu-id="21228-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="21228-112">トランスポート プロバイダーによって追加された可能性が最も高い文字は無視されます。</span><span class="sxs-lookup"><span data-stu-id="21228-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="21228-113">MAPI では、次の表で説明するように、RTF を操作する複数のプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="21228-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="21228-114">**RTF プロパティ**</span><span class="sxs-lookup"><span data-stu-id="21228-114">**RTF property**</span></span>|<span data-ttu-id="21228-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="21228-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21228-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21228-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21228-117">実際のメッセージ テキストの先頭を示します。</span><span class="sxs-lookup"><span data-stu-id="21228-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="21228-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21228-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21228-119">メッセージ テキストの循環冗長チェックの結果を格納します。</span><span class="sxs-lookup"><span data-stu-id="21228-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="21228-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21228-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21228-121">ファイル内の文字数が含 **PR_RTF_SYNC_BODY_CRC。**</span><span class="sxs-lookup"><span data-stu-id="21228-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="21228-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21228-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21228-123">メッセージ テキストと書式設定が同期されている場合は TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="21228-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="21228-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21228-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21228-125">メッセージ テキストの前に含まれる空白以外の文字の数を格納します。</span><span class="sxs-lookup"><span data-stu-id="21228-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="21228-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21228-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21228-127">メッセージ テキストを記録する空白以外の文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21228-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

