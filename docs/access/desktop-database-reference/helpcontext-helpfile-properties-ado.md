---
title: helpcontext プロパティと HelpFile プロパティ (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291993"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="3dfc0-102">helpcontext プロパティと HelpFile プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3dfc0-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="3dfc0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3dfc0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3dfc0-104">[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。</span><span class="sxs-lookup"><span data-stu-id="3dfc0-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="3dfc0-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="3dfc0-105">Return values</span></span>

- <span data-ttu-id="3dfc0-106">**HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。</span><span class="sxs-lookup"><span data-stu-id="3dfc0-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="3dfc0-107">**HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 (**String**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="3dfc0-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dfc0-108">注釈</span><span class="sxs-lookup"><span data-stu-id="3dfc0-108">Remarks</span></span>

<span data-ttu-id="3dfc0-p101">**HelpFile** プロパティでヘルプ ファイルが指定されている場合、**HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、**HelpContext** プロパティは 0 を返し、**HelpFile** プロパティは長さ 0 の文字列 ("") を返します。</span><span class="sxs-lookup"><span data-stu-id="3dfc0-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

