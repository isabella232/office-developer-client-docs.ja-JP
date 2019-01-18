---
title: ADO の列挙定数
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707942"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="75b24-102">ADO の列挙定数</span><span class="sxs-lookup"><span data-stu-id="75b24-102">ADO enumerated constants</span></span>

<span data-ttu-id="75b24-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="75b24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75b24-p101">ここでは、デバッグ用に各定数の実際の値の一覧を示します。ただし、この値は参考用のものであり、ADO のリリースごとに変更されることがあります。コードを記述するときは、列挙定数の実際の値ではなく、名前のみを使って記述するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="75b24-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="75b24-107">列挙型定数</span><span class="sxs-lookup"><span data-stu-id="75b24-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="75b24-108">説明</span><span class="sxs-lookup"><span data-stu-id="75b24-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="75b24-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-110">RDS の <strong>Recordset</strong> オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="75b24-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-112"><strong>MSDataShape</strong>プロバイダーが再階層<strong>レコード セット</strong>内の集計と集計の列を計算すると指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="75b24-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-114"><strong>Recordset</strong> オブジェクトを使用してデータ ソース行の共有的更新を行う際に、競合の検出に使用するフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="75b24-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-116"><strong>UpdateBatch</strong> メソッドに暗黙の <strong>Resync</strong> メソッド操作が続くかどうかを示し、続く場合はその操作の適用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-118">操作の対象となるレコードを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-120">操作の開始位置を示すブックマークを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-122">コマンド引数の解釈方法を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-124">ブックマークで表された 2 つのレコードの相対位置を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-126"><strong>Connection</strong> 内のデータの編集、 <strong>Record</strong> のオープン、または <strong>Record</strong> および <strong>Stream</strong> オブジェクトの <strong>Mode</strong> プロパティの値の指定に対する権限を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-128"><strong>Connection</strong> オブジェクトの <strong>Open</strong> メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-130">ODBC データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-132"><strong>CopyRecord</strong> メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-134">カーソル エンジンの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-136"><strong>Supports</strong> メソッドがテストする機能を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-138"><strong>Recordset</strong> オブジェクトが使用するカーソルの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-140"><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-142">レコードの編集状況を示します。</span><span class="sxs-lookup"><span data-stu-id="75b24-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-144">ADO 実行時エラーの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-146">イベントが発生した理由を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-148">イベントの実行の現在の状態を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-150">プロバイダーによるコマンドの実行方法を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-152"><strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションで参照される特定のフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-154"><strong>Field</strong> オブジェクトの 1 つ以上の属性を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-156"><strong>Field</strong> オブジェクトの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-158"><strong>Recordset</strong> でフィルターの対象となるレコード グループを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-160"><strong>Recordset</strong> から取得するレコード数を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-162"><strong>Connection</strong> オブジェクトのトランザクション分離レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-164">テキスト <strong>Stream</strong> オブジェクトの行区切り記号に使われている文字を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-166">編集時にレコードに適用されるロックの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-168">サーバーにどのレコードが返されるかを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-170"><strong>Record</strong> オブジェクトの <strong>MoveRecord</strong> メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-172">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-174"><strong>Parameter</strong> オブジェクトの属性を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-176"><strong>Parameter</strong> が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-178"><strong>Recordset</strong> を保存するときの形式を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-180"><strong>Recordset</strong> 内のレコード ポインターの現在の位置を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-182"><strong>Property</strong> オブジェクトの属性を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-184"><strong>Record</strong> オブジェクトの <strong>Open</strong> メソッドに対して、既存の <strong>Record</strong> を開くか、新しい <strong>Record</strong> を作成するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-p102"><strong>Record</strong> を開くときのオプションを指定します。これらの値は OR 演算子で結合することもできます。</span><span class="sxs-lookup"><span data-stu-id="75b24-p102">Specifies options for opening a <strong>Record</strong>. These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-189">バッチ更新またはその他の一括操作に関するレコードの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-191"><strong>Record</strong> オブジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-193"><strong>Resync</strong> の呼び出しによって基になる値が上書きされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-p103"><strong>Stream</strong> オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="75b24-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-p104"><strong>OpenSchema</strong> メソッドが取得するスキーマ <strong>Recordset</strong> の種類を指定します。<strong>Recordset</strong> 内のレコードの検索方向を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-p104">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves. Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-201"><strong>レコード セット</strong>内のレコードの検索の方向を指定します。実行する<strong>Seek</strong>の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-203">実行する<strong>Seek</strong>の種類を指定します。<strong>Stream</strong>オブジェクトを開くためのオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-203">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="75b24-204">これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="75b24-204">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-206"><strong>Stream</strong> オブジェクトを開くときのオプションを表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-206">Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="75b24-207">値は、AND 演算子で結合することができます。ストリーム全体、または次の行を<strong>ストリーム</strong>オブジェクトから読み取る必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-207">The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-209">ストリーム全体、または次の行を<strong>ストリーム</strong>オブジェクトから読み取る必要があるかどうかを指定します。<strong>Stream</strong>オブジェクトに格納されたデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-211"><strong>Stream</strong>オブジェクトに格納されたデータの種類を指定します。<strong>ストリーム</strong>オブジェクトに書き込む文字列を行区切り記号を追加するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-213"><strong>ストリーム</strong>オブジェクトに書き込む文字列を行区切り記号を追加するかどうかを指定します。文字列として<strong>Recordset</strong>を取得するときに形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b24-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-215">文字列として<strong>Recordset</strong>を取得するときに形式を指定します。<strong>Connection</strong>オブジェクトのトランザクション属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b24-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b24-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="75b24-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="75b24-217"><strong>Connection</strong> オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="75b24-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

