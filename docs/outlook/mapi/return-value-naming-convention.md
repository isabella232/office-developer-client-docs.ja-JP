---
title: 名前付け規則の値を返す
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 990a48c661621a3a704236a850f5d09239a12fca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803783"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="50f96-103">名前付け規則の値を返す</span><span class="sxs-lookup"><span data-stu-id="50f96-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="50f96-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50f96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50f96-105">MAPICODE。H ヘッダー ファイルには、多くのクライアントまたはサービス プロバイダーはインターフェイス メソッドの実装から返すことがありますか、呼び出しから返される可能性があります参照してください値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50f96-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="50f96-106">警告とエラーの状態を表すためのコードは、MAPI のプレフィックス、アンダー スコア、および W またはコードの種類を示すために E で始まる別の名前付け規則に従います。</span><span class="sxs-lookup"><span data-stu-id="50f96-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="50f96-107">コードの残りの部分は、条件を記述する短い文字列です。</span><span class="sxs-lookup"><span data-stu-id="50f96-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="50f96-108">文字列内の各単語は、アンダー スコアで区切られます。</span><span class="sxs-lookup"><span data-stu-id="50f96-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="50f96-109">たとえば、エラー値 MAPI_E_TOO_COMPLEX は、その実装に処理できませんでした呼び出しで要求されたどのようなを示します。</span><span class="sxs-lookup"><span data-stu-id="50f96-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="50f96-110">警告値 MAPI_W_PARTIAL_COMPLETION は、呼び出しが成功したことが、問題が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="50f96-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="50f96-111">操作の一部だけが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="50f96-111">Only part of the operation was completed successfully.</span></span>
  

