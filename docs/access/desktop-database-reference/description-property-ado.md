---
title: Description プロパティ (ADO)
TOCTitle: Description Property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3837d60b58772bbe6b65af6673c4eaa471507e66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476977"
---
# <a name="description-property-ado"></a><span data-ttu-id="09e7e-102">Description プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="09e7e-102">Description Property (ADO)</span></span>


<span data-ttu-id="09e7e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="09e7e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="09e7e-104">[Error](error-object-ado.md) オブジェクトを記述します。</span><span class="sxs-lookup"><span data-stu-id="09e7e-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="09e7e-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="09e7e-105">Return Value</span></span>

<span data-ttu-id="09e7e-106">エラーの内容を表す文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="09e7e-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e7e-107">解説</span><span class="sxs-lookup"><span data-stu-id="09e7e-107">Remarks</span></span>

<span data-ttu-id="09e7e-p101">**Description** プロパティは、エラーの簡単な説明を取得するために使います。プログラムで対処できないエラー、または処理することが望ましくないエラーは、このプロパティの内容を表示してユーザーに警告します。文字列は、ADO またはプロバイダーから渡されます。</span><span class="sxs-lookup"><span data-stu-id="09e7e-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="09e7e-p102">プロバイダーは、特定のエラー テキストを ADO に渡します。ADO は、受け取ったプロバイダー エラーまたは警告ごとに [Error](error-object-ado.md) オブジェクトを **Errors** コレクションに追加します。プロバイダーが渡すエラーをトレースするには、 **Errors** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="09e7e-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

