---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799719"
---
# <a name="attowner"></a><span data-ttu-id="3de2d-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="3de2d-103">attOwner</span></span>

  
  
<span data-ttu-id="3de2d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3de2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3de2d-105">**AttOwner**属性は、文字列の配置のエンド ・ ツー ・ エンドのようにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="3de2d-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="3de2d-106">**AttOwner**の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3de2d-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="3de2d-107">**attOwner**。</span><span class="sxs-lookup"><span data-stu-id="3de2d-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="3de2d-108">_電子メール アドレス_の表示名のアドレスと長さの表示名の長さ</span><span class="sxs-lookup"><span data-stu-id="3de2d-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="3de2d-109">_電子メール アドレス_</span><span class="sxs-lookup"><span data-stu-id="3de2d-109">_email-address_</span></span>
  
> <span data-ttu-id="3de2d-110">**::** の種類のアドレス</span><span class="sxs-lookup"><span data-stu-id="3de2d-110">type **:** address</span></span> 
    
<span data-ttu-id="3de2d-111">その他の長さとは異なり値、表示名の長さ、およびアドレスの長さは、符号なし長整数ではなく符号なしの 16 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="3de2d-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="3de2d-112">ただし終端の null 文字の場合は、それらも含まれます。</span><span class="sxs-lookup"><span data-stu-id="3de2d-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="3de2d-113">_電子メール アドレス_のエントリの種類とアドレスの文字列は、"smtp:joe@nowhere.com"などのリテラル コロン (:) 文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="3de2d-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="3de2d-114">のみ、組み合わされた型 **::** アドレス文字列には null で終わるです。</span><span class="sxs-lookup"><span data-stu-id="3de2d-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="3de2d-115">**AttOwner**属性に、MAPI プロパティのマッピングは、エンコードされているメッセージのメッセージ クラスに依存します。</span><span class="sxs-lookup"><span data-stu-id="3de2d-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

