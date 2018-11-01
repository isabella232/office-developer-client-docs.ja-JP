---
title: ADO の列挙定数
TOCTitle: ADO Enumerated Constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e9944138dcdca49f33ca293a9bdf41d88d86e9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882309"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="54e2f-102">ADO の列挙定数</span><span class="sxs-lookup"><span data-stu-id="54e2f-102">ADO Enumerated Constants</span></span>


<span data-ttu-id="54e2f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="54e2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54e2f-p101">ここでは、デバッグ用に各定数の実際の値の一覧を示します。ただし、この値は参考用のものであり、ADO のリリースごとに変更されることがあります。コードを記述するときは、列挙定数の実際の値ではなく、名前のみを使って記述するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="54e2f-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-107"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-107"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-108">RDS の <strong>Recordset</strong> オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-108">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-109"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-109"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-110"><strong>MSDataShape</strong>プロバイダーが再階層<strong>レコード セット</strong>内の集計と集計の列を計算すると指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-110">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-111"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-111"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-112"><strong>Recordset</strong> オブジェクトを使用してデータ ソース行の共有的更新を行う際に、競合の検出に使用するフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-112">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-113"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-113"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-114"><strong>UpdateBatch</strong> メソッドに暗黙の <strong>Resync</strong> メソッド操作が続くかどうかを示し、続く場合はその操作の適用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-114">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-115"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-115"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-116">操作の対象となるレコードを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-116">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-117"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-117"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-118">操作の開始位置を示すブックマークを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-118">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-119"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-119"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-120">コマンド引数の解釈方法を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-120">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-121"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-121"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-122">ブックマークで表された 2 つのレコードの相対位置を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-122">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-123"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-123"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-124"><strong>Connection</strong> 内のデータの編集、 <strong>Record</strong> のオープン、または <strong>Record</strong> および <strong>Stream</strong> オブジェクトの <strong>Mode</strong> プロパティの値の指定に対する権限を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-124">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-125"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-125"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-126"><strong>Connection</strong> オブジェクトの <strong>Open</strong> メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-126">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-127"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-127"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-128">ODBC データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-128">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-129"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-129"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-130"><strong>CopyRecord</strong> メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-130">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-131"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-131"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-132">カーソル エンジンの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-132">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-133"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-133"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-134"><strong>Supports</strong> メソッドがテストする機能を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-134">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-135"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-135"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-136"><strong>Recordset</strong> オブジェクトが使用するカーソルの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-136">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-137"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-137"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-138"><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-138">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-139"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-139"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-140">レコードの編集状況を示します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-140">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-141"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-141"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-142">ADO 実行時エラーの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-142">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-143"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-143"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-144">イベントが発生した理由を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-144">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-145"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-145"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-146">イベントの実行の現在の状態を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-146">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-147"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-147"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-148">プロバイダーによるコマンドの実行方法を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-148">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-149"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-149"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-150"><strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションで参照される特定のフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-150">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-151"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-151"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-152"><strong>Field</strong> オブジェクトの 1 つ以上の属性を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-152">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-153"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-153"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-154"><strong>Field</strong> オブジェクトの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-154">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-155"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-155"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-156"><strong>Recordset</strong> でフィルターの対象となるレコード グループを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-156">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-157"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-157"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-158"><strong>Recordset</strong> から取得するレコード数を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-158">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-159"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-159"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-160"><strong>Connection</strong> オブジェクトのトランザクション分離レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-160">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-161"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-161"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-162">テキスト <strong>Stream</strong> オブジェクトの行区切り記号に使われている文字を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-162">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-163"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-163"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-164">編集時にレコードに適用されるロックの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-164">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-165"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-165"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-166">サーバーにどのレコードが返されるかを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-166">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-167"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-167"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-168"><strong>Record</strong> オブジェクトの <strong>MoveRecord</strong> メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-168">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-169"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-169"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-170">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-170">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-171"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-171"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-172"><strong>Parameter</strong> オブジェクトの属性を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-172">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-173"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-173"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-174"><strong>Parameter</strong> が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-174">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-175"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-175"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-176"><strong>Recordset</strong> を保存するときの形式を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-176">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-177"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-177"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-178"><strong>Recordset</strong> 内のレコード ポインターの現在の位置を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-178">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-179"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-179"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-180"><strong>Property</strong> オブジェクトの属性を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-180">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-181"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-181"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-182"><strong>Record</strong> オブジェクトの <strong>Open</strong> メソッドに対して、既存の <strong>Record</strong> を開くか、新しい <strong>Record</strong> を作成するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-182">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-183"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-183"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-p102"><strong>Record</strong> を開くときのオプションを指定します。これらの値は OR 演算子で結合することもできます。</span><span class="sxs-lookup"><span data-stu-id="54e2f-p102">Specifies options for opening a <strong>Record</strong>. These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-186"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-186"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-187">バッチ更新またはその他の一括操作に関するレコードの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-187">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-188"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-188"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-189"><strong>Record</strong> オブジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-189">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-190"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-190"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-191"><strong>Resync</strong> の呼び出しによって基になる値が上書きされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-191">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-192"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-192"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-p103"><strong>Stream</strong> オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="54e2f-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-195"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-195"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-p104"><strong>OpenSchema</strong> メソッドが取得するスキーマ <strong>Recordset</strong> の種類を指定します。<strong>Recordset</strong> 内のレコードの検索方向を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-p104">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves. Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-198"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-198"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-199"><strong>レコード セット</strong>内のレコードの検索の方向を指定します。実行する<strong>Seek</strong>の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-199">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-200"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-200"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-201">実行する<strong>Seek</strong>の種類を指定します。<strong>Stream</strong>オブジェクトを開くためのオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-201">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="54e2f-202">これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="54e2f-202">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-203"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-203"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-204"><strong>Stream</strong> オブジェクトを開くときのオプションを表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-204">Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="54e2f-205">値は、AND 演算子で結合することができます。ストリーム全体、または次の行を<strong>ストリーム</strong>オブジェクトから読み取る必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-205">The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-206"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-206"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-207">ストリーム全体、または次の行を<strong>ストリーム</strong>オブジェクトから読み取る必要があるかどうかを指定します。<strong>Stream</strong>オブジェクトに格納されたデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-207">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-208"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-208"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-209"><strong>Stream</strong>オブジェクトに格納されたデータの種類を指定します。<strong>ストリーム</strong>オブジェクトに書き込む文字列を行区切り記号を追加するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-209">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-210"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-210"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-211"><strong>ストリーム</strong>オブジェクトに書き込む文字列を行区切り記号を追加するかどうかを指定します。文字列として<strong>Recordset</strong>を取得するときに形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-211">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54e2f-212"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-212"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-213">文字列として<strong>Recordset</strong>を取得するときに形式を指定します。<strong>Connection</strong>オブジェクトのトランザクション属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-213">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54e2f-214"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="54e2f-214"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="54e2f-215"><strong>Connection</strong> オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="54e2f-215">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

