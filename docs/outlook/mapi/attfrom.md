---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6460cd3ef0495a5494e03b4c7034e067cf8793b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576065"
---
# <a name="attfrom"></a><span data-ttu-id="01185-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="01185-103">attFrom</span></span>

<span data-ttu-id="01185-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01185-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01185-105">**AttFrom**属性は、表示名と、必要なスペースの後に、送信者のアドレスの後に、送信者の表示名と電子メール アドレスをエンコードする**TRP**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="01185-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="01185-106">**AttFrom**の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="01185-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="01185-107">**attFrom**: 送信者の表示名 _ 送信者アドレス _ パディングの_TRP 構造_</span><span class="sxs-lookup"><span data-stu-id="01185-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="01185-108">送信者の表示名では、null で終わる文字列を null 文字を追加、必要に応じて、2 バイト境界に到達します。</span><span class="sxs-lookup"><span data-stu-id="01185-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="01185-109">**AttFrom**エンコーディングの末尾のスペースは、 **sizeof(TRP)** の境界に到達するために必要な null 文字で構成されます。</span><span class="sxs-lookup"><span data-stu-id="01185-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="01185-110">_TRP 構造:_**trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="01185-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="01185-111">**AttFrom**アイテム、 **TRP**の-構造体は常に、1 回限りのエンコーディングをそのため**TRP**から trpid の構造体のフィールドは、常に**trpidOneOff**。</span><span class="sxs-lookup"><span data-stu-id="01185-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="01185-112">Cbgrtrp や cch、cb の項目は、 **TRP**の構造体の残りのフィールドに対応します。</span><span class="sxs-lookup"><span data-stu-id="01185-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="01185-113">Cbgrtrp フィールドは、の合計として計算 **(sizeof(TRP) \*2)** の null で終わる送信者の表示名、パディング、長さ、null で終端された送信者のアドレスの長さ。</span><span class="sxs-lookup"><span data-stu-id="01185-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="01185-114">Cch フィールドは、そのスペースを持つ null で終わる表示名の長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="01185-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="01185-115">Cb フィールドは、null で終端された送信者のアドレスの長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="01185-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="01185-116">_送信者アドレス:_ **::** のアドレスの種類 **'\0'** を解決します。</span><span class="sxs-lookup"><span data-stu-id="01185-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="01185-117">送信者アドレスは、4 つの部分、アドレスの種類が、リテラルのコロン (:)、アドレス自体、および終端の null 文字で構成される文字列です。</span><span class="sxs-lookup"><span data-stu-id="01185-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="01185-118">文字列では、 `fax:1-909-555-1234\0` 、有効な送信者アドレスの値になります。</span><span class="sxs-lookup"><span data-stu-id="01185-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

