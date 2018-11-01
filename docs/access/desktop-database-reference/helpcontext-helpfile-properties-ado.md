---
title: HelpContext プロパティと HelpFile プロパティ (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a9ad8c700b0b0ae293683f7b79062a0edf7775f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881371"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="5041d-102">HelpContext プロパティと HelpFile プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="5041d-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="5041d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5041d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5041d-104">[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。</span><span class="sxs-lookup"><span data-stu-id="5041d-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="5041d-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="5041d-105">Return values</span></span>

- <span data-ttu-id="5041d-106">**HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。</span><span class="sxs-lookup"><span data-stu-id="5041d-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="5041d-107">**HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="5041d-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="5041d-108">解説</span><span class="sxs-lookup"><span data-stu-id="5041d-108">Remarks</span></span>

<span data-ttu-id="5041d-p101">**HelpFile** プロパティでヘルプ ファイルが指定されている場合、 **HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、 **HelpContext** プロパティは 0 を返し、 **HelpFile** プロパティは長さ 0 の文字列 ("") を返します。</span><span class="sxs-lookup"><span data-stu-id="5041d-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

