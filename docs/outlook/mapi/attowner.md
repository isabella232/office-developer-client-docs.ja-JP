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
# <a name="attowner"></a><span data-ttu-id="dafcc-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="dafcc-103">attOwner</span></span>

  
  
<span data-ttu-id="dafcc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dafcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dafcc-105">**attOwner**属性は、エンドツーエンドで配置された、カウントされた文字列としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="dafcc-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="dafcc-106">**attOwner**の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dafcc-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="dafcc-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="dafcc-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="dafcc-108">表示名-長さの表示-名前アドレスの長さの_電子メールアドレス_</span><span class="sxs-lookup"><span data-stu-id="dafcc-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="dafcc-109">_電子メールアドレス_</span><span class="sxs-lookup"><span data-stu-id="dafcc-109">_email-address_</span></span>
  
> <span data-ttu-id="dafcc-110">型 **:** address</span><span class="sxs-lookup"><span data-stu-id="dafcc-110">type **:** address</span></span> 
    
<span data-ttu-id="dafcc-111">他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なしの長い整数ではなく、符号なしの16ビットの値になります。</span><span class="sxs-lookup"><span data-stu-id="dafcc-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="dafcc-112">ただし、終端の null 文字はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="dafcc-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="dafcc-113">_電子メールアドレス_エントリの type および address 文字列は、リテラルのコロン (:) で区切られています。文字 ("smtp:joe@nowhere.com" など)。</span><span class="sxs-lookup"><span data-stu-id="dafcc-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="dafcc-114">結合された型 **:** address 文字列は null で終了します。</span><span class="sxs-lookup"><span data-stu-id="dafcc-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="dafcc-115">MAPI プロパティの**attOwner**属性へのマッピングは、エンコードされるメッセージのメッセージクラスに依存します。</span><span class="sxs-lookup"><span data-stu-id="dafcc-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

