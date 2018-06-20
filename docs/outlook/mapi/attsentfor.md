---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799739"
---
# <a name="attsentfor"></a><span data-ttu-id="4de7d-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="4de7d-103">attSentFor</span></span>

  
  
<span data-ttu-id="4de7d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4de7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4de7d-105">**AttSentFor**属性は、文字列の配置のエンド ・ ツー ・ エンドのようにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="4de7d-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="4de7d-106">**AttSentFor**の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4de7d-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="4de7d-107">**attSentFor**。</span><span class="sxs-lookup"><span data-stu-id="4de7d-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="4de7d-108">_電子メール アドレス_の表示名のアドレスと長さの表示名の長さ</span><span class="sxs-lookup"><span data-stu-id="4de7d-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="4de7d-109">_電子メール アドレス_</span><span class="sxs-lookup"><span data-stu-id="4de7d-109">_email-address_</span></span>
  
> <span data-ttu-id="4de7d-110">**::** の種類のアドレス</span><span class="sxs-lookup"><span data-stu-id="4de7d-110">type **:** address</span></span> 
    
<span data-ttu-id="4de7d-111">その他の長さとは異なり値、表示名の長さ、およびアドレスの長さは、符号なし長整数ではなく符号なしの 16 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="4de7d-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="4de7d-112">ただし終端の null 文字の場合は、それらも含まれます。</span><span class="sxs-lookup"><span data-stu-id="4de7d-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="4de7d-113">_電子メール アドレス_のエントリの種類とアドレスの文字列は、"smtp:joe@nowhere.com"などのリテラル コロン (:) 文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="4de7d-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="4de7d-114">のみ、組み合わされた型 **::** アドレス文字列には null で終わるです。</span><span class="sxs-lookup"><span data-stu-id="4de7d-114">Only the combined type **:** address string is null-terminated.</span></span>
  

