---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799721"
---
# <a name="attmessagestatus"></a><span data-ttu-id="96145-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="96145-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="96145-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96145-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96145-105">MAPI メッセージのフラグは、下位互換性を保持するためにフラグを TNEF にマップされます。</span><span class="sxs-lookup"><span data-stu-id="96145-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="96145-106">すべてのフラグがグループ化され、1 バイトでエンコードします。</span><span class="sxs-lookup"><span data-stu-id="96145-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="96145-107">マッピングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="96145-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="96145-108">**MAPI メッセージのフラグ**</span><span class="sxs-lookup"><span data-stu-id="96145-108">**MAPI message flags**</span></span>|<span data-ttu-id="96145-109">**TNEF フラグ**</span><span class="sxs-lookup"><span data-stu-id="96145-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96145-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="96145-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="96145-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="96145-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="96145-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="96145-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="96145-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="96145-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="96145-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="96145-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="96145-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="96145-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="96145-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="96145-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="96145-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="96145-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="96145-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="96145-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="96145-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="96145-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="96145-120">TNEF では、これらのフラグが定義されています。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="96145-120">These flags are defined in the TNEF.H header file.</span></span>
  

