---
title: 戻り値の名前付け規則
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423616"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="a2fc7-103">戻り値の名前付け規則</span><span class="sxs-lookup"><span data-stu-id="a2fc7-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="a2fc7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2fc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2fc7-105">MAPICODE。H ヘッダー ファイルには、クライアントまたはサービス プロバイダーがインターフェイス メソッドの実装から返す値、または呼び出しから返される可能性がある値の多くが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="a2fc7-106">警告とエラーの条件を表すコードは、プレフィックス MAPI、アンダースコア、およびコードの種類を示す W または E で始まる別の名前付け規則に従います。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="a2fc7-107">残りのコードは、条件を記述する短い文字列です。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="a2fc7-108">文字列内の各単語はアンダースコアで区切ります。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="a2fc7-109">たとえば、呼び出しで要求MAPI_E_TOO_COMPLEX処理できないというエラー値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="a2fc7-110">警告の値MAPI_W_PARTIAL_COMPLETION呼び出しが成功したが、問題が発生したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="a2fc7-111">操作の一部だけが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="a2fc7-111">Only part of the operation was completed successfully.</span></span>
  

