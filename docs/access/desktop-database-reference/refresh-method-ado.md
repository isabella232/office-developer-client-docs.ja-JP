---
title: Refresh メソッド (ADO)
TOCTitle: Refresh Method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ea277f83c39bde4b5309a26b87961ff2325b145
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476446"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="37d49-102">Refresh メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="37d49-102">Refresh Method (ADO)</span></span>


<span data-ttu-id="37d49-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="37d49-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37d49-104">コレクションのオブジェクトを更新し、プロバイダーから使用可能な、プロバイダーに固有のオブジェクトを反映します。</span><span class="sxs-lookup"><span data-stu-id="37d49-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d49-105">構文</span><span class="sxs-lookup"><span data-stu-id="37d49-105">Syntax</span></span>

<span data-ttu-id="37d49-106">*コレクション*です。更新</span><span class="sxs-lookup"><span data-stu-id="37d49-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="37d49-107">解説</span><span class="sxs-lookup"><span data-stu-id="37d49-107">Remarks</span></span>

<span data-ttu-id="37d49-108">**Refresh** メソッドは、どのコレクションから呼び出すかによって異なる操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="37d49-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="37d49-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37d49-109">Parameters</span></span>

<span data-ttu-id="37d49-p101">**Command** オブジェクトの [Parameters](command-object-ado.md) コレクションで [Refresh](parameters-collection-ado.md) メソッドを使用すると、 **Command** オブジェクトで指定されたストアド プロシージャまたはパラメーター化されたクエリに関するプロバイダー側のパラメーター情報が取得されます。プロバイダーがストアド プロシージャの呼び出しまたはパラメーター化されたクエリをサポートしない場合には、コレクションは空になります。</span><span class="sxs-lookup"><span data-stu-id="37d49-p101">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object. The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="37d49-112">[Refresh](activeconnection-property-ado.md) メソッドを呼び出す前に、 **Command** オブジェクトの [ActiveConnection](connection-object-ado.md) プロパティを有効な [Connection](commandtext-property-ado.md) オブジェクトに、 [CommandText](commandtype-property-ado.md) プロパティを有効なコマンドに、 **CommandType** プロパティを **adCmdStoredProc** に、それぞれ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d49-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="37d49-113">**Refresh** メソッドを呼び出す前に **Parameters** コレクションにアクセスすると、自動的にメソッドが呼び出され、コレクションが更新されます。</span><span class="sxs-lookup"><span data-stu-id="37d49-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>


> [!NOTE]
> <P><span data-ttu-id="37d49-p102">[!メモ] <STRONG>Refresh</STRONG> メソッドを使用してプロバイダーからパラメーター情報を取得し、1 つまたは複数の可変長データ型の <A href="parameter-object-ado.md">Parameter</A> オブジェクトが返される場合、ADO はパラメーターの最大可能サイズに基づいてメモリを割り当てるため、実行時にエラーが発生します。エラーを避けるには、 <A href="size-property-ado.md">Execute</A> メソッドを呼び出す前に、これらのパラメーターの <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Size</A> プロパティを明示的に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d49-p102">If you use the <STRONG>Refresh</STRONG> method to obtain parameter information from the provider and it returns one or more variable-length data type <A href="parameter-object-ado.md">Parameter</A> objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the <A href="size-property-ado.md">Size</A> property for these parameters before calling the <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> method to prevent errors.</span></span></P>



<span data-ttu-id="37d49-116">**Fields**</span><span class="sxs-lookup"><span data-stu-id="37d49-116">**Fields**</span></span>

<span data-ttu-id="37d49-p103">**Fields** コレクションに対して **Refresh** メソッドを使用しても、目に見える効果はありません。基になっているデータベース構造から変更を取得するには、 [Requery](requery-method-ado.md) メソッドを使用するか、または [Recordset](recordset-object-ado.md) オブジェクトがブックマークをサポートしない場合は [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d49-p103">Using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="37d49-119">**Properties**</span><span class="sxs-lookup"><span data-stu-id="37d49-119">**Properties**</span></span>

<span data-ttu-id="37d49-p104">一部のオブジェクトの **Properties** コレクションに対して **Refresh** メソッドを使用すると、プロバイダーが公開するダイナミック プロパティでコレクションが作成されます。このようなプロパティは、ADO がサポートする組み込みプロパティにはない、プロバイダーに固有の機能に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="37d49-p104">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes. These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>
