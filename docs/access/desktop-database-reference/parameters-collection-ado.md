---
title: Parameters コレクション (ADO)
TOCTitle: Parameters Collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7a1da73679bd63de0c35362b87b2db8259698614
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867791"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="d93bc-102">Parameters コレクション (ADO)</span><span class="sxs-lookup"><span data-stu-id="d93bc-102">Parameters Collection (ADO)</span></span>


<span data-ttu-id="d93bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d93bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d93bc-104">[Command](parameter-object-ado.md) オブジェクトのすべての [Parameter](command-object-ado.md) オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="d93bc-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d93bc-105">備考</span><span class="sxs-lookup"><span data-stu-id="d93bc-105">Remarks</span></span>

<span data-ttu-id="d93bc-106">**Command** オブジェクトには、 **Parameter** オブジェクトから構成される **Parameters** コレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="d93bc-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="d93bc-p101">[Command](refresh-method-ado.md) オブジェクトの **Parameters** コレクションで **Refresh** メソッドを使用すると、 **Command** オブジェクトで指定されたストアド プロシージャまたはパラメーター化されたクエリに関するプロバイダー側のパラメーター情報が取得されます。プロバイダーの中には、ストアド プロシージャの呼び出しまたはパラメーター化されたクエリをサポートしないものもあります。このようなプロバイダーを使用する場合、 **Parameters** コレクションの **Refresh** メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d93bc-p101">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object. Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="d93bc-109">独自の **Parameter** オブジェクトを定義せず、 **Refresh** メソッドを呼び出す前に **Parameters** コレクションにアクセスすると、自動的にメソッドが呼び出され、コレクションが更新されます。</span><span class="sxs-lookup"><span data-stu-id="d93bc-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="d93bc-p102">呼び出すストアド プロシージャまたはパラメーター化されたクエリに関連するパラメーターのプロパティを把握していると、プロバイダーの呼び出しを最小限に抑えて、パフォーマンスを向上させることができます。[CreateParameter](createparameter-method-ado.md) メソッドを使用して適切なプロパティ設定を備えた **Parameter** オブジェクトを作成し、 [Append](append-method-ado.md) メソッドを使用してそれらのオブジェクトを **Parameters** コレクションに追加します。これにより、プロバイダーを呼び出してパラメーター情報を取得しなくても、パラメーターの値を設定したり返したりすることができます。パラメーター情報を提供しないプロバイダーに書き込む場合にパラメーターを使用するには、このメソッドを使用して手動で **Parameters** コレクションを設定する必要があります。 [Delete](delete-method-ado-parameters-collection.md) メソッドを使用すると、必要に応じて **Parameters** コレクションから **Parameter** オブジェクトを削除できます。</span><span class="sxs-lookup"><span data-stu-id="d93bc-p102">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call. Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all. Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="d93bc-115">**Recordset** の **Parameters** コレクションのオブジェクトは、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="d93bc-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

