---
title: Size プロパティ (ADO)
TOCTitle: Size Property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b690bd735f01e077b52c13c6c6e9b478234c1e8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479004"
---
# <a name="size-property-ado"></a><span data-ttu-id="410c2-102">Size プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="410c2-102">Size Property (ADO)</span></span>


<span data-ttu-id="410c2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="410c2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="410c2-104">[Parameter](parameter-object-ado.md) オブジェクトの最大サイズをバイト数または文字数で示します。</span><span class="sxs-lookup"><span data-stu-id="410c2-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="410c2-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="410c2-105">Settings and Return Values</span></span>

<span data-ttu-id="410c2-106">**Parameter** オブジェクトの最大サイズをバイト数または文字数で示す長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="410c2-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="410c2-107">解説</span><span class="sxs-lookup"><span data-stu-id="410c2-107">Remarks</span></span>

<span data-ttu-id="410c2-108">**Parameter** オブジェクトの [Value](value-property-ado.md) プロパティで設定または取得できる値の最大サイズを調べるには、 **Size** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="410c2-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="410c2-109">**Parameter** オブジェクトとして可変長データ型 (たとえば、**adVarChar** などのすべての文字列型 (**String**)) を指定した場合、[Parameters](parameters-collection-ado.md) コレクションにそのオブジェクトを追加する前に、オブジェクトの **Size** プロパティを設定する必要があり、この設定を行わないとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="410c2-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="410c2-110">**Parameter** オブジェクトが **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションに既に追加されている場合に、そのデータ型を可変長データ型に変更した場合は、 **Command** オブジェクトを実行する前に **Parameter** オブジェクトの **Size** プロパティを設定する必要があり、この設定を行わないとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="410c2-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="410c2-p101">[Refresh](refresh-method-ado.md) メソッドを使用してプロバイダーからパラメーター情報を取得したときに、可変長データ型の **Parameter** オブジェクトが返された場合、可能な最大サイズに基づいてパラメーターにメモリが割り当てられますが、これが原因で実行時にエラーが発生することがあります。エラーを回避するには、コマンドを実行する前に、明示的にこれらのパラメーターの **Size** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="410c2-p101">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution. To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="410c2-113">**Size** プロパティは、値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="410c2-113">The **Size** property is read/write.</span></span>

