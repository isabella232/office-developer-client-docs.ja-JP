---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427655"
---
# <a name="attowner"></a><span data-ttu-id="f5268-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="f5268-103">attOwner</span></span>

  
  
<span data-ttu-id="f5268-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5268-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5268-105">**attOwner 属性** は、エンドツーエンドに配置されたカウントされた文字列としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="f5268-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="f5268-106">**attOwner の形式は** 次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f5268-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="f5268-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="f5268-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="f5268-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="f5268-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="f5268-109">_電子メール アドレス_</span><span class="sxs-lookup"><span data-stu-id="f5268-109">_email-address_</span></span>
  
> <span data-ttu-id="f5268-110">type **:** address</span><span class="sxs-lookup"><span data-stu-id="f5268-110">type **:** address</span></span> 
    
<span data-ttu-id="f5268-111">他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なし長整数ではなく、符号なし 16 ビットの値です。</span><span class="sxs-lookup"><span data-stu-id="f5268-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="f5268-112">ただし、null 文字の終端は引き続き含まれます。</span><span class="sxs-lookup"><span data-stu-id="f5268-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="f5268-113">電子メール アドレス エントリ内の型とアドレスの文字列は、リテラルコロン (:)"smtp:joe@nowhere.com" などの文字。</span><span class="sxs-lookup"><span data-stu-id="f5268-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="f5268-114">結合された型 **: アドレス** 文字列だけが null 終端です。</span><span class="sxs-lookup"><span data-stu-id="f5268-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="f5268-115">MAPI プロパティと **attOwner** 属性のマッピングは、エンコードされるメッセージのメッセージ クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f5268-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

