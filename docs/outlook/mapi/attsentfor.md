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
# <a name="attsentfor"></a><span data-ttu-id="99cd1-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="99cd1-103">attSentFor</span></span>

  
  
<span data-ttu-id="99cd1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99cd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99cd1-105">属性**の添付文**は、エンドツーエンドで配置された文字列のカウントとしてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="99cd1-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="99cd1-106">**添付**ファイルの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="99cd1-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="99cd1-107">**添付の対象**:</span><span class="sxs-lookup"><span data-stu-id="99cd1-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="99cd1-108">表示名-長さの表示-名前アドレスの長さの_電子メールアドレス_</span><span class="sxs-lookup"><span data-stu-id="99cd1-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="99cd1-109">_電子メールアドレス_</span><span class="sxs-lookup"><span data-stu-id="99cd1-109">_email-address_</span></span>
  
> <span data-ttu-id="99cd1-110">型 **:** address</span><span class="sxs-lookup"><span data-stu-id="99cd1-110">type **:** address</span></span> 
    
<span data-ttu-id="99cd1-111">他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なしの長い整数ではなく、符号なしの16ビットの値になります。</span><span class="sxs-lookup"><span data-stu-id="99cd1-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="99cd1-112">ただし、終端の null 文字はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="99cd1-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="99cd1-113">_電子メールアドレス_エントリの type および address 文字列は、リテラルのコロン (:) で区切られています。文字 ("smtp:joe@nowhere.com" など)。</span><span class="sxs-lookup"><span data-stu-id="99cd1-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="99cd1-114">結合された型 **:** address 文字列は null で終了します。</span><span class="sxs-lookup"><span data-stu-id="99cd1-114">Only the combined type **:** address string is null-terminated.</span></span>
  

