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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432416"
---
# <a name="attfrom"></a><span data-ttu-id="ecd1e-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="ecd1e-103">attFrom</span></span>

<span data-ttu-id="ecd1e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecd1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecd1e-105">**attFrom** 属性は、送信者の表示名と電子メール アドレスをエンコードし、その後に送信者の表示名とアドレスをエンコードし、その後に必要な埋め込みを行う **TRP** 構造としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="ecd1e-106">**attFrom の形式は** 次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="ecd1e-107">**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding</span><span class="sxs-lookup"><span data-stu-id="ecd1e-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="ecd1e-108">sender-display-name は、2 バイト境界に到達するために、必要に応じて追加の null 文字が埋め込まれます。null 終端文字列です。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="ecd1e-109">**attFrom** エンコードの末尾のパディングは **、sizeof(TRP)** 境界に到達するために必要な数の null 文字で構成されます。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="ecd1e-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="ecd1e-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="ecd1e-111">**attFrom** アイテムの **場合、TRP**-structure は常に 1 回限りエンコードなので **、TRP**-structure フィールドの trpid は常に **trpidOneOff** です。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="ecd1e-112">cbgrtrp、cch、cb アイテムは **、TRP** 構造の残りのフィールドに対応します。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="ecd1e-113">cbgrtrp フィールドは、合計 **(sizeof(TRP) \* 2)、** 埋め込み値を持つ null 終端の送信者表示名の長さ、および null 終端の送信者アドレスの長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="ecd1e-114">cch フィールドは、余白を持つ null 終端表示名の長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="ecd1e-115">cb フィールドは、null 終端の送信者アドレスの長さとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="ecd1e-116">_sender-address:_ address-type **:** address **'\0'**</span><span class="sxs-lookup"><span data-stu-id="ecd1e-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="ecd1e-117">送信者アドレスは、アドレスの種類、リテラルコロン (:)、アドレス自体、および終端の null 文字) の 4 つの部分で構成される文字列です。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="ecd1e-118">たとえば、文字列は `fax:1-909-555-1234\0` 、合法的な送信者アドレス値になります。</span><span class="sxs-lookup"><span data-stu-id="ecd1e-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

