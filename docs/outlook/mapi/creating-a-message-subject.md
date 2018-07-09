---
title: メッセージの件名を作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799872"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="768f2-103">メッセージの件名を作成します。</span><span class="sxs-lookup"><span data-stu-id="768f2-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="768f2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="768f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="768f2-105">**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))、メッセージの件名は、メッセージの目的を要約するために使用、省略可能なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="768f2-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="768f2-106">設定する場合は、文字列を作成して文字 128 バイト以内です。</span><span class="sxs-lookup"><span data-stu-id="768f2-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="768f2-107">128 バイトの制限は、MAPI のによって課された制限ではありません。いくつかのメッセージ ストア プロバイダーによって課された制限することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="768f2-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="768f2-108">それを課すはプロバイダーとの相互運用性を確保するには、サブジェクトが 128 バイトに制限します。</span><span class="sxs-lookup"><span data-stu-id="768f2-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="768f2-109">いくつかのメッセージ ストア プロバイダーは、 [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx)インターフェイスを使用して、ストリームに書き込むために**あるの PR_SUBJECT**を許可しないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="768f2-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="768f2-110">**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) は設定されていませんこのプロパティが応答でのみ設定され、メッセージを転送しました。</span><span class="sxs-lookup"><span data-stu-id="768f2-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

