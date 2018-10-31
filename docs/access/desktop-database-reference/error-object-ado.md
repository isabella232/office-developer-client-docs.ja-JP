---
title: エラー オブジェクト、ActiveX データ オブジェクト (ADO)
TOCTitle: Error Object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38fa73120ed868c7b7a0e086cdcbe822e4c16730
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860988"
---
# <a name="error-object-ado"></a><span data-ttu-id="23546-102">Error オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="23546-102">Error Object (ADO)</span></span>


<span data-ttu-id="23546-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="23546-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23546-104">プロバイダーを含む単一の操作に関連して発生した、データ アクセス エラーの詳細情報を格納しています。</span><span class="sxs-lookup"><span data-stu-id="23546-104">Contains details about data access errors that pertain to a single operation involving the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="23546-105">備考</span><span class="sxs-lookup"><span data-stu-id="23546-105">Remarks</span></span>

<span data-ttu-id="23546-p101">ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが [Connection](errors-collection-ado.md) オブジェクトの [Errors](connection-object-ado.md) コレクションに追加されます。別の ADO 操作でエラーが発生すると、 **Errors** コレクションがクリアされ、 **Error** オブジェクトの新しいセットが **Errors** コレクションに配置されます。</span><span class="sxs-lookup"><span data-stu-id="23546-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the [Errors](errors-collection-ado.md) collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="23546-p102">[!メモ] 各 **Error** オブジェクトは、ADO エラーではなく特定のプロバイダー エラーを表します。ADO エラーは、実行時の例外処理メカニズムに公開されます。たとえば、Microsoft Visual Basic の場合、ADO 固有のエラーが発生すると、 **On Error** イベントが実行され、そのエラーが **Error** オブジェクトに追加されます。ADO エラーをすべて記載した一覧については、 [ErrorValueEnum](errorvalueenum.md) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23546-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an **On Error** event and appear in the **Error** object. For a complete list of ADO errors, see the [ErrorValueEnum](errorvalueenum.md) topic.</span></span>

<span data-ttu-id="23546-113">各エラーの詳細については、次のプロパティを含む **Error** オブジェクトのプロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23546-113">You can read an **Error** object's properties to obtain specific details about each error, including the following:</span></span>

- <span data-ttu-id="23546-p103">エラーのテキストを格納する、[Description](description-property-ado.md) プロパティ。これは既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="23546-p103">The [Description](description-property-ado.md) property, which contains the text of the error. This is the default property.</span></span>

- <span data-ttu-id="23546-116">エラー定数の長整数型 ( [Long](number-property-ado.md) ) の値を格納する、 **Number** プロパティ。</span><span class="sxs-lookup"><span data-stu-id="23546-116">The [Number](number-property-ado.md) property, which contains the **Long** integer value of the error constant.</span></span>

- <span data-ttu-id="23546-p104">エラーの発生源となったオブジェクトを特定する、[Source](source-property-ado-error.md) プロパティ。特にデータ ソースに対する要求に続いて、 **Errors** コレクションに複数の **Error** オブジェクトが追加された場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="23546-p104">The [Source](source-property-ado-error.md) property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to a data source.</span></span>

- <span data-ttu-id="23546-119">SQL データ ソースの情報を提供する、[SQLState](sqlstate-property-ado.md) プロパティと [NativeError](nativeerror-property-ado.md) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="23546-119">The [SQLState](sqlstate-property-ado.md) and [NativeError](nativeerror-property-ado.md) properties, which provide information from SQL data sources.</span></span>

<span data-ttu-id="23546-p105">プロバイダー エラーは発生すると、 **Connection** オブジェクトの **Errors** コレクションに追加されます。ADO では 1 回の ADO 操作で複数のエラーを取得できるため、プロバイダー固有のエラー情報を見込んでおくことができます。エラー ハンドラーにあるこうした豊富なエラー情報を取得するには、使用している言語や環境の適切なエラー トラッピング機能を使用し、ネストされたループで **Errors** コレクションの各 **Error** オブジェクトのプロパティを列挙します。</span><span class="sxs-lookup"><span data-stu-id="23546-p105">When a provider error occurs, it is placed in the **Errors** collection of the **Connection** object. ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider. To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each **Error** object in the **Errors** collection.</span></span>

<span data-ttu-id="23546-123">**Microsoft Visual Basic および VBScript ユーザー**有効な**接続**オブジェクトがない場合、 **Error**オブジェクトからエラー情報を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23546-123">**Microsoft Visual Basic and VBScript Users**If there is no valid **Connection** object, you will need to retrieve error information from the **Error** object.</span></span>

<span data-ttu-id="23546-p106">ADO は、プロバイダーと同様に、新たなプロバイダー エラーを発生させる可能性がある呼び出しを行う前に、 **OLE Error Info** オブジェクトをクリアします。ただし、 **Connection** オブジェクトの **Errors** コレクションがクリアされ、オブジェクトが追加されるのは、プロバイダーで新しいエラーが生成されるか、 [Clear](clear-method-ado.md) メソッドを呼び出す場合のみです。</span><span class="sxs-lookup"><span data-stu-id="23546-p106">Just as providers do, ADO clears the **OLE Error Info** object before making a call that could potentially generate a new provider error. However, the **Errors** collection on the **Connection** object is cleared and populated only when the provider generates a new error, or when the [Clear](clear-method-ado.md) method is called.</span></span>

<span data-ttu-id="23546-p107">プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで **Open** メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="23546-p107">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a **Connection** object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

