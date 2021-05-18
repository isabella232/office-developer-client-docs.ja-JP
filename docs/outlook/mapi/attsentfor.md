---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408839"
---
# <a name="attsentfor"></a><span data-ttu-id="9d67d-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="9d67d-103">attSentFor</span></span>

  
  
<span data-ttu-id="9d67d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d67d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d67d-105">**attSentFor** 属性は、エンドツーエンドに配置されたカウントされた文字列としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="9d67d-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="9d67d-106">**attSentFor の形式は** 次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d67d-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="9d67d-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="9d67d-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="9d67d-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="9d67d-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="9d67d-109">_電子メール アドレス_</span><span class="sxs-lookup"><span data-stu-id="9d67d-109">_email-address_</span></span>
  
> <span data-ttu-id="9d67d-110">type **:** address</span><span class="sxs-lookup"><span data-stu-id="9d67d-110">type **:** address</span></span> 
    
<span data-ttu-id="9d67d-111">他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なし長整数ではなく、符号なし 16 ビットの値です。</span><span class="sxs-lookup"><span data-stu-id="9d67d-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="9d67d-112">ただし、null 文字の終端は引き続き含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d67d-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="9d67d-113">電子メール アドレス エントリ内の型とアドレスの文字列は、リテラルコロン (:)"smtp:joe@nowhere.com" などの文字。</span><span class="sxs-lookup"><span data-stu-id="9d67d-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="9d67d-114">結合された型 **: アドレス** 文字列だけが null 終端です。</span><span class="sxs-lookup"><span data-stu-id="9d67d-114">Only the combined type **:** address string is null-terminated.</span></span>
  

