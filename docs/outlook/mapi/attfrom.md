---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318159"
---
# <a name="attfrom"></a><span data-ttu-id="55b6c-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="55b6c-103">attFrom</span></span>

<span data-ttu-id="55b6c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55b6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55b6c-105">この\*\*\*\* 属性は、送信者の表示名と電子メールアドレス、送信者の表示名とアドレス、および必要なスペースをエンコードする**trp**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="55b6c-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="55b6c-106">**添付**ファイルの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="55b6c-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="55b6c-107">**添付元**: _trp 構造_送信者-表示名 _ 送信者-アドレス _ padding</span><span class="sxs-lookup"><span data-stu-id="55b6c-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="55b6c-108">送信者の表示名は、null で終了する文字列で、必要に応じて2バイト境界になるまで、追加の null 文字が埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="55b6c-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="55b6c-109">**添付**文字の末尾のスペースは、 **sizeof (trp)** 境界に到達するために必要な数の null 文字で構成されます。</span><span class="sxs-lookup"><span data-stu-id="55b6c-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="55b6c-110">_trp 構造:_**trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="55b6c-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="55b6c-111">[**添付**] アイテムの場合、 **trp**構造は常に1回限りのエンコードであるため、trp 構造\*\*\*\* フィールドからの trp は常に**trpidOneOff**になります。</span><span class="sxs-lookup"><span data-stu-id="55b6c-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="55b6c-112">cbgrtrp、cch、および cb の各項目は、 **trp**構造体の残りのフィールドに対応しています。</span><span class="sxs-lookup"><span data-stu-id="55b6c-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="55b6c-113">cbgrtrp フィールドは、合計 **(sizeof (trp) \*2)**、null で終了する送信者の表示名の長さと、null で終了する送信者のアドレスの長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="55b6c-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="55b6c-114">cch フィールドは、スペースを含む null で終わる表示名の長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="55b6c-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="55b6c-115">cb フィールドは、null で終了する送信者アドレスの長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="55b6c-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="55b6c-116">_sender-address:_ address-type **:** address **' \ 0 '**</span><span class="sxs-lookup"><span data-stu-id="55b6c-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="55b6c-117">送信者のアドレスは、アドレスの種類、リテラルのコロン (:)、アドレス自体、終端の null 文字で構成される、4つの部分で構成される文字列です。</span><span class="sxs-lookup"><span data-stu-id="55b6c-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="55b6c-118">たとえば、文字列`fax:1-909-555-1234\0`は法的な送信者アドレスの値になります。</span><span class="sxs-lookup"><span data-stu-id="55b6c-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

