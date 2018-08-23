---
title: テキストと書式設定の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588819"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="f1d3d-103">テキストと書式設定の同期</span><span class="sxs-lookup"><span data-stu-id="f1d3d-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="f1d3d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1d3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1d3d-105">リッチ テキスト形式 (RTF) メッセージを送信する主な課題には、テキストの書式設定と同期し続けることです。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="f1d3d-106">されることを確認メッセージが送信先に到着すると、発信者の意図とすると、テキストと書式設定の同期はを MAPI に[行う](rtfsync.md)機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="f1d3d-107">**** 通常と呼ばれる受信したメッセージを表示する前に、rtf 形式に対応していないクライアントと、MAPI スプーラーによってトランスポート プロバイダーにメッセージをダウンロードする際です。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="f1d3d-108">呼び出しを**行う**1 つまたは 2 つのフラグを渡すことによって可能な不一致の領域を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="f1d3d-109">メッセージ テキスト内の変更箇所を示すために RTF_SYNC_BODY_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="f1d3d-110">メッセージの書式設定の変更を示すために RTF_SYNC_RTF_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="f1d3d-111">**** で発生する同期プロセスは、いくつかの文字を無視し、他のユーザーに変換するメッセージのテキストの高度な巡回冗長検査 (CRC)。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="f1d3d-112">ほとんどの場合、トランスポート プロバイダーによって追加された文字は無視されます。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="f1d3d-113">MAPI は、次の表で説明したように、rtf 形式を使用するためのいくつかのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="f1d3d-114">**RTF プロパティ**</span><span class="sxs-lookup"><span data-stu-id="f1d3d-114">**RTF property**</span></span>|<span data-ttu-id="f1d3d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="f1d3d-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1d3d-116">**PR_RTF_SYNC_BODY_TAG**([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f1d3d-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d3d-117">実際のメッセージ テキストの先頭を示します。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="f1d3d-118">**PR_RTF_SYNC_BODY_CRC**([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f1d3d-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d3d-119">メッセージ テキストの巡回冗長検査の結果が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="f1d3d-120">**PR_RTF_SYNC_BODY_COUNT**([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f1d3d-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d3d-121">**PR_RTF_SYNC_BODY_CRC**の文字数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="f1d3d-122">**PR_RTF_IN_SYNC**([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f1d3d-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d3d-123">場合は、TRUE に設定、メッセージ テキストと書式設定が同期されています。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="f1d3d-124">**PR_RTF_SYNC_PREFIX_COUNT**([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f1d3d-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d3d-125">メッセージ テキストを撤廃する nonwhitespace の文字数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="f1d3d-126">**PR_RTF_SYNC_TRAILING_COUNT**([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f1d3d-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f1d3d-127">メッセージのテキストを記録する nonwhitespace の文字数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1d3d-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

