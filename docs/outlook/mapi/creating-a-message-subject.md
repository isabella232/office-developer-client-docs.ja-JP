---
title: メッセージ件名の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332964"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="73400-103">メッセージ件名の作成</span><span class="sxs-lookup"><span data-stu-id="73400-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="73400-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73400-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73400-105">メッセージの件名である PR_SUBJECT **(** [PidTagSubject)](pidtagsubject-canonical-property.md)は、メッセージの意図を要約するために使用されるオプションのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="73400-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="73400-106">設定する場合は、文字列を 128 バイト以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="73400-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="73400-107">128 バイトの制限は、MAPI によって課される制限ではありません。これは、一部のメッセージ ストア プロバイダーによって課される制限です。</span><span class="sxs-lookup"><span data-stu-id="73400-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="73400-108">これを行うプロバイダーとの相互運用性を確保するには、サブジェクトを 128 バイトに制限します。</span><span class="sxs-lookup"><span data-stu-id="73400-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="73400-109">一部のメッセージ ストア プロバイダーでは、IStream インターフェイスPR_SUBJECTストリームへの書き込みが許可されていない[場合](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)があります。 </span><span class="sxs-lookup"><span data-stu-id="73400-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="73400-110">[設定しない **] PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md));このプロパティは、返信と転送されたメッセージにのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="73400-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

