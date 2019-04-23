---
title: NextRecordset メソッド (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b572f4ebe55da1add781ecd86df97937cfeae126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288618"
---
# <a name="nextrecordset-method-ado"></a><span data-ttu-id="4ae11-102">NextRecordset メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="4ae11-102">NextRecordset method (ADO)</span></span>

<span data-ttu-id="4ae11-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ae11-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="4ae11-104">現在の [Recordset](recordset-object-ado.md) オブジェクトをクリアし、一連のコマンド操作を実行して次の **Recordset** を返します。</span><span class="sxs-lookup"><span data-stu-id="4ae11-104">Clears the current [Recordset](recordset-object-ado.md) object and returns the next **Recordset** by advancing through a series of commands.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae11-105">構文</span><span class="sxs-lookup"><span data-stu-id="4ae11-105">Syntax</span></span>

<span data-ttu-id="4ae11-106">*recordset2* = *recordset1*を設定します。NextRecordset (*RecordsAffected* )</span><span class="sxs-lookup"><span data-stu-id="4ae11-106">Set *recordset2* = *recordset1*.NextRecordset(*RecordsAffected* )</span></span>

## <a name="return-value"></a><span data-ttu-id="4ae11-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="4ae11-107">Return value</span></span>

<span data-ttu-id="4ae11-p101">**Recordset** オブジェクトを返します。構文モデルの *recordset1* と *recordset2* には、同じ **Recordset** オブジェクト、または別のオブジェクトを指定できます。別の **Recordset** オブジェクトを使用する場合、**NextRecordset** の呼び出しの後に元の **Recordset** (*recordset1*) の **ActiveConnection** プロパティを再設定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4ae11-p101">Returns a **Recordset** object. In the syntax model, *recordset1* and *recordset2* can be the same **Recordset** object, or you can use separate objects. When using separate **Recordset** objects, resetting the **ActiveConnection** property on the original **Recordset** (*recordset1*) after **NextRecordset** has been called will generate an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ae11-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4ae11-111">Parameters</span></span>

|<span data-ttu-id="4ae11-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4ae11-112">Parameter</span></span>|<span data-ttu-id="4ae11-113">説明</span><span class="sxs-lookup"><span data-stu-id="4ae11-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4ae11-114">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="4ae11-114">*RecordsAffected*</span></span> |<span data-ttu-id="4ae11-p102">省略可能です。長整数型 ( **Long** ) の変数を指定します。プロバイダーは、操作の影響を受けたレコード数をここに返します。</span><span class="sxs-lookup"><span data-stu-id="4ae11-p102">Optional. A **Long** variable to which the provider returns the number of records that the current operation affected.</span></span>|

> [!NOTE]
> <span data-ttu-id="4ae11-117">このパラメーターは、操作の影響を受けたレコード数のみを返します。**Recordset** を作成するために使用された Select ステートメントからのレコード数を返すことはありません。</span><span class="sxs-lookup"><span data-stu-id="4ae11-117">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae11-118">注釈</span><span class="sxs-lookup"><span data-stu-id="4ae11-118">Remarks</span></span>

<span data-ttu-id="4ae11-119">**NextRecordset** メソッドでは、複合コマンド ステートメントの次のコマンドの結果、または複数の結果を返すストアド プロシージャの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="4ae11-119">Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</span></span> <span data-ttu-id="4ae11-120">複合コマンドステートメントに基づいて**Recordset**オブジェクトを開いた場合 (たとえば、"table1 から\*選択してください。[ \* table2 からの選択][コマンド](command-object-ado.md)に対して[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドまたは**recordset**の[Open](open-method-ado-recordset.md)メソッドを使用すると、最初のコマンドのみが実行され、結果が*recordset*に返されます。</span><span class="sxs-lookup"><span data-stu-id="4ae11-120">If you open a **Recordset** object based on a compound command statement (for example, "SELECT \* FROM table1;SELECT \* FROM table2") using the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*.</span></span> <span data-ttu-id="4ae11-121">ステートメントの次のコマンドの結果にアクセスするには、 **NextRecordset** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4ae11-121">To access the results of subsequent commands in the statement, call the **NextRecordset** method.</span></span>

<span data-ttu-id="4ae11-122">その他の結果があり、複合ステートメントを含む**Recordset**がプロセス境界を越えて切断またはマーシャリングされていない限り、 **NextRecordset**メソッドは引き続き**recordset**オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4ae11-122">As long as there are additional results and the **Recordset** containing the compound statements is not disconnected or marshaled across process boundaries, the **NextRecordset** method will continue to return **Recordset** objects.</span></span> <span data-ttu-id="4ae11-123">行を返すコマンドが正常に実行されてもレコードが返されない場合は、返された**Recordset**オブジェクトが空になります。</span><span class="sxs-lookup"><span data-stu-id="4ae11-123">If a row-returning command executes successfully but returns no records, the returned **Recordset** object will be open but empty.</span></span> <span data-ttu-id="4ae11-124">この場合は、 [BOF](bof-eof-properties-ado.md)プロパティと[EOF](bof-eof-properties-ado.md)プロパティが両方とも**True**であることを確認してテストします。</span><span class="sxs-lookup"><span data-stu-id="4ae11-124">Test for this case by verifying that the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties are both **True**.</span></span> <span data-ttu-id="4ae11-125">行を返さないコマンドが正常に実行された場合は、返された**recordset**オブジェクトが閉じられ、 **recordset**の[State](state-property-ado.md)プロパティをテストすることによって確認できます。</span><span class="sxs-lookup"><span data-stu-id="4ae11-125">If a non–row-returning command executes successfully, the returned **Recordset** object will be closed, which you can verify by testing the [State](state-property-ado.md) property on the **Recordset**.</span></span> <span data-ttu-id="4ae11-126">結果がなければ、 *recordset*は*Nothing*に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4ae11-126">When there are no more results, *recordset* will be set to *Nothing*.</span></span>

<span data-ttu-id="4ae11-127">切断された **Recordset** オブジェクトでは、 **ActiveConnection** が [Nothing](activeconnection-property-ado.md) (Microsoft Visual Basic) または NULL (その他の言語) に設定されているため、 **NextRecordset** メソッドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="4ae11-127">The **NextRecordset** method is not available on a disconnected **Recordset** object, where [ActiveConnection](activeconnection-property-ado.md) has been set to **Nothing** (in Microsoft Visual Basic) or NULL (in other languages).</span></span>

<span data-ttu-id="4ae11-128">即時更新モードで編集を行っているときに **NextRecordset** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ae11-128">If an edit is in progress while in immediate update mode, calling the **NextRecordset** method generates an error; call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span>

<span data-ttu-id="4ae11-p105">複合ステートメントの複数のコマンドにパラメーターを渡すには、[Parameters](parameters-collection-ado.md) コレクションを使用するか、または元の **Open** メソッドまたは **Execute** メソッドの呼び出しで配列を渡します。この場合、コレクションまたは配列のパラメーターの並び順は、一連のコマンドの並び順と同じである必要があります。出力パラメーターの値を読み込むには、すべての結果の読み込みが終了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ae11-p105">To pass parameters for more than one command in the compound statement by filling the [Parameters](parameters-collection-ado.md) collection, or by passing an array with the original **Open** or **Execute** call, the parameters must be in the same order in the collection or array as their respective commands in the command series. You must finish reading all the results before reading output parameter values.</span></span>

<span data-ttu-id="4ae11-p106">複合ステートメント内の各コマンドをいつ実行するかは、OLE DB プロバイダーが決定します。たとえば、[Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) は、複合ステートメントを受け取ったときにすべてのコマンドをバッチで実行します。結果の **Recordsets** は、 **NextRecordset** を呼び出したときに返されます。</span><span class="sxs-lookup"><span data-stu-id="4ae11-p106">Your OLE DB provider determines when each command command in a compound statement is executed. The [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), for example, executes all commands in a batch upon receiving the compound statement. The resulting **Recordsets** are simply returned when you call **NextRecordset**.</span></span>

<span data-ttu-id="4ae11-p107">ただし、それ以外のプロバイダーでは、ステートメント内の次のコマンドが NextRecordset の呼び出しの後にしか実行されないこともあります。そのようなプロバイダーの場合、ステートメントのすべてのコマンドを実行する前に **Recordset** オブジェクトを明示的に閉じると、残りのコマンドは実行されません。</span><span class="sxs-lookup"><span data-stu-id="4ae11-p107">However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.</span></span>

