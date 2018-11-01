---
title: NextRecordset メソッド (ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec6b6677e0de89b22f3c35009edcbc05684d10ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872600"
---
# <a name="nextrecordset-method-ado"></a><span data-ttu-id="4135f-102">NextRecordset メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="4135f-102">NextRecordset Method (ADO)</span></span>


<span data-ttu-id="4135f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4135f-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="4135f-104">現在の [Recordset](recordset-object-ado.md) オブジェクトをクリアし、一連のコマンド操作を実行して次の **Recordset** を返します。</span><span class="sxs-lookup"><span data-stu-id="4135f-104">Clears the current [Recordset](recordset-object-ado.md) object and returns the next **Recordset** by advancing through a series of commands.</span></span>

## <a name="syntax"></a><span data-ttu-id="4135f-105">構文</span><span class="sxs-lookup"><span data-stu-id="4135f-105">Syntax</span></span>

<span data-ttu-id="4135f-106">*Recordset2*の設定 = *recordset1*。NextRecordset (*RecordsAffected* )</span><span class="sxs-lookup"><span data-stu-id="4135f-106">Set *recordset2* = *recordset1*.NextRecordset(*RecordsAffected* )</span></span>

## <a name="return-value"></a><span data-ttu-id="4135f-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="4135f-107">Return value</span></span>

<span data-ttu-id="4135f-p101">**Recordset** オブジェクトを返します。構文モデルの *recordset1* と *recordset2* には、同じ **Recordset** オブジェクト、または別のオブジェクトを指定できます。別の **Recordset** オブジェクトを使用する場合、**NextRecordset** の呼び出しの後に元の **Recordset** (*recordset1*) の **ActiveConnection** プロパティを再設定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4135f-p101">Returns a **Recordset** object. In the syntax model, *recordset1* and *recordset2* can be the same **Recordset** object, or you can use separate objects. When using separate **Recordset** objects, resetting the **ActiveConnection** property on the original **Recordset** (*recordset1*) after **NextRecordset** has been called will generate an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="4135f-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4135f-111">Parameters</span></span>

- <span data-ttu-id="4135f-112">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="4135f-112">*RecordsAffected*</span></span>

- <span data-ttu-id="4135f-p102">省略可能です。長整数型 ( **Long** ) の変数を指定します。プロバイダーは、操作の影響を受けたレコード数をここに返します。</span><span class="sxs-lookup"><span data-stu-id="4135f-p102">Optional. A **Long** variable to which the provider returns the number of records that the current operation affected.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4135f-115">[!メモ] このパラメーターは、操作の影響を受けたレコード数のみを返します。 <STRONG>Recordset</STRONG> を作成するために使用された Select ステートメントからのレコード数を返すことはありません。</span><span class="sxs-lookup"><span data-stu-id="4135f-115">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <STRONG>Recordset</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="4135f-116">解説</span><span class="sxs-lookup"><span data-stu-id="4135f-116">Remarks</span></span>

<span data-ttu-id="4135f-117">**NextRecordset** メソッドでは、複合コマンド ステートメントの次のコマンドの結果、または複数の結果を返すストアド プロシージャの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="4135f-117">Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</span></span> <span data-ttu-id="4135f-118">複合コマンド ステートメントに基づく**レコード セット**オブジェクトを開くかどうか (たとえば、"を選択して\*table1; から\* Table2 から」) [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドを使用して、[コマンド](command-object-ado.md)または**レコード セット**で[Open](open-method-ado-recordset.md)メソッドで、ADO は最初のコマンドのみを実行し、*レコード セット*に結果を返します。</span><span class="sxs-lookup"><span data-stu-id="4135f-118">If you open a **Recordset** object based on a compound command statement (for example, "SELECT \* FROM table1;SELECT \* FROM table2") using the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*.</span></span> <span data-ttu-id="4135f-119">ステートメントの次のコマンドの結果にアクセスするには、 **NextRecordset** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4135f-119">To access the results of subsequent commands in the statement, call the **NextRecordset** method.</span></span>

<span data-ttu-id="4135f-120">追加の結果は、複合ステートメントを含む**レコード セット**が切断またはプロセスの境界を越えてマーシャ リングされない限り、 **NextRecordset**メソッドは引き続き**レコード セット**オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4135f-120">As long as there are additional results and the **Recordset** containing the compound statements is not disconnected or marshaled across process boundaries, the **NextRecordset** method will continue to return **Recordset** objects.</span></span> <span data-ttu-id="4135f-121">行を返すコマンドが正常に実行されるレコードが返されない場合は、返された**Recordset**オブジェクトが開いている空れます。</span><span class="sxs-lookup"><span data-stu-id="4135f-121">If a row-returning command executes successfully but returns no records, the returned **Recordset** object will be open but empty.</span></span> <span data-ttu-id="4135f-122">このケースをテストするには、 [bof プロパティ](bof-eof-properties-ado.md)と[EOF](bof-eof-properties-ado.md)プロパティが両方の**場合は True**であることの確認します。</span><span class="sxs-lookup"><span data-stu-id="4135f-122">Test for this case by verifying that the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties are both **True**.</span></span> <span data-ttu-id="4135f-123">行を返さないコマンドが正常に実行された場合、返される**レコード セット**オブジェクトは閉じて**レコード セット**で、 [State](state-property-ado.md)プロパティをテストすることによって確認することができます。</span><span class="sxs-lookup"><span data-stu-id="4135f-123">If a non–row-returning command executes successfully, the returned **Recordset** object will be closed, which you can verify by testing the [State](state-property-ado.md) property on the **Recordset**.</span></span> <span data-ttu-id="4135f-124">以上結果が存在する場合、*レコード セット*を*Nothing*に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4135f-124">When there are no more results, *recordset* will be set to *Nothing*.</span></span>

<span data-ttu-id="4135f-125">切断された **Recordset** オブジェクトでは、 **ActiveConnection** が [Nothing](activeconnection-property-ado.md) (Microsoft Visual Basic) または NULL (その他の言語) に設定されているため、 **NextRecordset** メソッドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="4135f-125">The **NextRecordset** method is not available on a disconnected **Recordset** object, where [ActiveConnection](activeconnection-property-ado.md) has been set to **Nothing** (in Microsoft Visual Basic) or NULL (in other languages).</span></span>

<span data-ttu-id="4135f-126">即時更新モードで編集を行っているときに **NextRecordset** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4135f-126">If an edit is in progress while in immediate update mode, calling the **NextRecordset** method generates an error; call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span>

<span data-ttu-id="4135f-p105">複合ステートメントの複数のコマンドにパラメーターを渡すには、[Parameters](parameters-collection-ado.md) コレクションを使用するか、または元の **Open** メソッドまたは **Execute** メソッドの呼び出しで配列を渡します。この場合、コレクションまたは配列のパラメーターの並び順は、一連のコマンドの並び順と同じである必要があります。出力パラメーターの値を読み込むには、すべての結果の読み込みが終了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4135f-p105">To pass parameters for more than one command in the compound statement by filling the [Parameters](parameters-collection-ado.md) collection, or by passing an array with the original **Open** or **Execute** call, the parameters must be in the same order in the collection or array as their respective commands in the command series. You must finish reading all the results before reading output parameter values.</span></span>

<span data-ttu-id="4135f-p106">複合ステートメント内の各コマンドをいつ実行するかは、OLE DB プロバイダーが決定します。たとえば、[Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) は、複合ステートメントを受け取ったときにすべてのコマンドをバッチで実行します。結果の **Recordsets** は、 **NextRecordset** を呼び出したときに返されます。</span><span class="sxs-lookup"><span data-stu-id="4135f-p106">Your OLE DB provider determines when each command command in a compound statement is executed. The [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), for example, executes all commands in a batch upon receiving the compound statement. The resulting **Recordsets** are simply returned when you call **NextRecordset**.</span></span>

<span data-ttu-id="4135f-p107">ただし、それ以外のプロバイダーでは、ステートメント内の次のコマンドが NextRecordset の呼び出しの後にしか実行されないこともあります。そのようなプロバイダーの場合、ステートメントのすべてのコマンドを実行する前に **Recordset** オブジェクトを明示的に閉じると、残りのコマンドは実行されません。</span><span class="sxs-lookup"><span data-stu-id="4135f-p107">However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.</span></span>

