---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799721"
---
# <a name="attmessagestatus"></a><span data-ttu-id="ad2d1-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ad2d1-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="ad2d1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad2d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad2d1-105">MAPI メッセージのフラグは、下位互換性を保持するためにフラグを TNEF にマップされます。</span><span class="sxs-lookup"><span data-stu-id="ad2d1-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="ad2d1-106">すべてのフラグがグループ化され、1 バイトでエンコードします。</span><span class="sxs-lookup"><span data-stu-id="ad2d1-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="ad2d1-107">マッピングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ad2d1-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="ad2d1-108">**MAPI メッセージのフラグ**</span><span class="sxs-lookup"><span data-stu-id="ad2d1-108">**MAPI message flags**</span></span>|<span data-ttu-id="ad2d1-109">**TNEF フラグ**</span><span class="sxs-lookup"><span data-stu-id="ad2d1-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad2d1-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="ad2d1-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="ad2d1-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="ad2d1-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="ad2d1-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="ad2d1-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="ad2d1-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="ad2d1-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="ad2d1-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="ad2d1-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="ad2d1-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="ad2d1-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="ad2d1-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="ad2d1-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="ad2d1-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="ad2d1-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="ad2d1-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="ad2d1-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="ad2d1-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="ad2d1-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="ad2d1-120">TNEF では、これらのフラグが定義されています。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="ad2d1-120">These flags are defined in the TNEF.H header file.</span></span>
  

