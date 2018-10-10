---
title: Parameter オブジェクト (ADO)
TOCTitle: Parameter Object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7667828d2ebfdc554a7120bf495374bc50e51cfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477028"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="dfc38-102">Parameter オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="dfc38-102">Parameter Object (ADO)</span></span>


<span data-ttu-id="dfc38-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfc38-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dfc38-104">パラメーター クエリまたはストアド プロシージャに基づく、[Command](command-object-ado.md) オブジェクトに関連付けられたパラメーターまたは引数を表します。</span><span class="sxs-lookup"><span data-stu-id="dfc38-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc38-105">備考</span><span class="sxs-lookup"><span data-stu-id="dfc38-105">Remarks</span></span>

<span data-ttu-id="dfc38-p101">プロバイダーの多くは、パラメーター化されたコマンドをサポートしています。これらのコマンドでは、必要なアクションが事前に定義されていますが、コマンドの一部の詳細を変更するために変数 (またはパラメーター) が使用されています。たとえば、SQL SELECT ステートメントでは、あるパラメーターを使用して WHERE 句の照合条件を定義し、別のパラメーターを使用して SORT BY 句の列名を定義できます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-p101">Many providers support parameterized commands. These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command. For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="dfc38-p102">**Parameter** オブジェクトは、パラメーター化されたクエリ、またはストアド プロシージャの入出力引数と戻り値に関連付けられたパラメーターを表します。プロバイダーの機能によっては、 **Parameter** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="dfc38-p102">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures. Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="dfc38-111">**Parameter** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="dfc38-112">[Name](name-property-ado.md) プロパティを使用して、パラメーターの名前を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="dfc38-p103">[Value](value-property-ado.md) プロパティを使用して、パラメーターの値を設定または取得できます。 **Value** は、 **Parameter** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="dfc38-p103">Set or return the value of a parameter with the [Value](value-property-ado.md) property. **Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="dfc38-115">[Attributes](attributes-property-ado.md)、[Direction](direction-property-ado.md)、[Precision](precision-property-ado.md)、[NumericScale](numericscale-property-ado.md)、[Size](size-property-ado.md)、および [Type](type-property-ado.md) の各プロパティを使用して、パラメーターの特性を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="dfc38-116">[AppendChunk](appendchunk-method-ado.md) メソッドを使用して、長いバイナリ データまたは文字データを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="dfc38-117">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有の属性にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="dfc38-p104">呼び出すストアド プロシージャまたはパラメーター化されたクエリに関連するパラメーターの名前とプロパティを把握している場合、[CreateParameter](createparameter-method-ado.md) メソッドを使用して、適切なプロパティが設定された **Parameter** オブジェクトを作成し、 [Append](append-method-ado.md) メソッドを使用して、それらのオブジェクトを [Parameters](parameters-collection-ado.md) コレクションに追加できます。これにより、 [Parameters](refresh-method-ado.md) コレクションの **Refresh** メソッドを呼び出してプロバイダーからパラメーター情報を取得しなくても、パラメーターの値を設定したり取得したりすることができるため、リソース消費量を少なくできます。</span><span class="sxs-lookup"><span data-stu-id="dfc38-p104">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

