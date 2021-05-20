---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430316"
---
# <a name="attmessagestatus"></a><span data-ttu-id="fcebd-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="fcebd-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="fcebd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcebd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcebd-105">MAPI メッセージ フラグは、下位互換性を維持するために TNEF フラグにマップされます。</span><span class="sxs-lookup"><span data-stu-id="fcebd-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="fcebd-106">すべてのフラグがグループ化され、1 バイトでエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="fcebd-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="fcebd-107">マッピングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fcebd-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="fcebd-108">**MAPI メッセージ フラグ**</span><span class="sxs-lookup"><span data-stu-id="fcebd-108">**MAPI message flags**</span></span>|<span data-ttu-id="fcebd-109">**TNEF フラグ**</span><span class="sxs-lookup"><span data-stu-id="fcebd-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcebd-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="fcebd-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="fcebd-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="fcebd-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="fcebd-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="fcebd-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="fcebd-113">~fmsModified</span><span class="sxs-lookup"><span data-stu-id="fcebd-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="fcebd-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="fcebd-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="fcebd-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="fcebd-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="fcebd-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="fcebd-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="fcebd-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="fcebd-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="fcebd-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="fcebd-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="fcebd-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="fcebd-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="fcebd-120">これらのフラグは TNEF で定義されます。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="fcebd-120">These flags are defined in the TNEF.H header file.</span></span>
  

