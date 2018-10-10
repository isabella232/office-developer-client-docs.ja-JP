---
title: HelpContext プロパティと HelpFile プロパティ (ADO)
TOCTitle: HelpContext, HelpFile Properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23823ec18b4b87306fa852ac5b0b18e89f60d057
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478891"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="c9297-102">HelpContext プロパティと HelpFile プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9297-102">HelpContext, HelpFile Properties (ADO)</span></span>


<span data-ttu-id="c9297-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9297-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9297-104">[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。</span><span class="sxs-lookup"><span data-stu-id="c9297-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9297-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9297-105">Return Values</span></span>

  - <span data-ttu-id="c9297-106">**HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。</span><span class="sxs-lookup"><span data-stu-id="c9297-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="c9297-107">**HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="c9297-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9297-108">解説</span><span class="sxs-lookup"><span data-stu-id="c9297-108">Remarks</span></span>

<span data-ttu-id="c9297-p101">**HelpFile** プロパティでヘルプ ファイルが指定されている場合、 **HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、 **HelpContext** プロパティは 0 を返し、 **HelpFile** プロパティは長さ 0 の文字列 ("") を返します。</span><span class="sxs-lookup"><span data-stu-id="c9297-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

