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
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565747"
---
# <a name="attmessagestatus"></a><span data-ttu-id="de6ca-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="de6ca-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="de6ca-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de6ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de6ca-105">MAPI メッセージのフラグは、下位互換性を保持するためにフラグを TNEF にマップされます。</span><span class="sxs-lookup"><span data-stu-id="de6ca-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="de6ca-106">すべてのフラグがグループ化され、1 バイトでエンコードします。</span><span class="sxs-lookup"><span data-stu-id="de6ca-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="de6ca-107">マッピングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="de6ca-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="de6ca-108">**MAPI メッセージのフラグ**</span><span class="sxs-lookup"><span data-stu-id="de6ca-108">**MAPI message flags**</span></span>|<span data-ttu-id="de6ca-109">**TNEF フラグ**</span><span class="sxs-lookup"><span data-stu-id="de6ca-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de6ca-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="de6ca-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="de6ca-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="de6ca-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="de6ca-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="de6ca-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="de6ca-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="de6ca-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="de6ca-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="de6ca-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="de6ca-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="de6ca-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="de6ca-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="de6ca-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="de6ca-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="de6ca-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="de6ca-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="de6ca-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="de6ca-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="de6ca-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="de6ca-120">TNEF では、これらのフラグが定義されています。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="de6ca-120">These flags are defined in the TNEF.H header file.</span></span>
  

