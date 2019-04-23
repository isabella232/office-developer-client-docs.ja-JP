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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283409"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="09eef-102">ADO の列挙定数</span><span class="sxs-lookup"><span data-stu-id="09eef-102">ADO enumerated constants</span></span>

<span data-ttu-id="09eef-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="09eef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09eef-p101">ここでは、デバッグ用に各定数の実際の値の一覧を示します。ただし、この値は参考用のものであり、ADO のリリースごとに変更されることがあります。コードを記述するときは、列挙定数の実際の値ではなく、名前のみを使って記述するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="09eef-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="09eef-107">列挙定数</span><span class="sxs-lookup"><span data-stu-id="09eef-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="09eef-108">説明</span><span class="sxs-lookup"><span data-stu-id="09eef-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="09eef-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-110">RDS の <strong>Recordset</strong> オブジェクトに対して、データを取得する非同期スレッドの実行優先順位を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="09eef-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-112">階層 <strong>Recordset</strong> の集計列と計算列を <strong>MSDataShape</strong> プロバイダーがいつ再計算するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="09eef-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-114"><strong>Recordset</strong> オブジェクトがあるデータ ソース行の共有的更新時に、競合の検出に使用するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="09eef-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-116"><strong>UpdateBatch</strong> メソッドに暗黙の <strong>Resync</strong> メソッド操作を実行するかどうか、実行する場合は、その操作の適用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-118">操作の対象となるレコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-120">操作の開始位置を示すブックマークを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-122">コマンド引数をどのように解釈するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-124">ブックマークで表された 2 つのレコードの相対位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-126"><strong>Connection</strong> 内のデータ編集、<strong>Record</strong> のオープン、または <strong>Record</strong> オブジェクトと <strong>Stream</strong> オブジェクトの <strong>Mode</strong> プロパティの値の指定に対する権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-128"><strong>Connection</strong> オブジェクトの <strong>Open</strong> メソッドからの戻りが、接続が確立された後 (同期) か前 (非同期) かを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-130">ODBC データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-132"><strong>CopyRecord</strong> メソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-134">カーソル エンジンの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-136"><strong>Supports</strong> メソッドがテストする機能を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-138"><strong>Recordset</strong> オブジェクトが使用するカーソルの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-140"><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-142">レコードの編集ステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-144">ADO 実行時エラーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-146">イベントが発生する理由を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-148">イベント実行のカレント ステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-150">プロバイダーによるコマンドの実行方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-152"><strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションで参照される特定のフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-154">1 つまたは複数の <strong>Field</strong> オブジェクトの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-156"><strong>Field</strong> オブジェクトのステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-158"><strong>Recordset</strong> でフィルターの対象となるレコード グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-160"><strong>Recordset</strong> から取得するレコード数を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-162"><strong>Connection</strong> オブジェクトのトランザクション分離レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-164">テキスト <strong>Stream</strong> オブジェクトの行区切り記号に使用されている文字を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-166">編集時にレコードに適用されるロックの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-168">サーバーにどのレコードが返されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-170"><strong>Record</strong> オブジェクトの <strong>MoveRecord</strong> メソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-172">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-174"><strong>Parameter</strong> オブジェクトの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-176"><strong>Parameter</strong> が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-178"><strong>Recordset</strong> を保存するときの形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-180"><strong>Recordset</strong> 内のレコード ポインターの現在の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-182"><strong>Property</strong> オブジェクトの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-184"><strong>Record</strong> オブジェクトの <strong>Open</strong> メソッドに対して、既存の <strong>Record</strong> を開くか、新しい <strong>Record</strong> を作成するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-186"><strong>Record</strong> を開くときのオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-186">Specifies options for opening a <strong>Record</strong>.</span></span> <span data-ttu-id="09eef-187">これらの値は OR 演算子で結合することもできます。</span><span class="sxs-lookup"><span data-stu-id="09eef-187">These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-189">バッチ更新または別の大量の操作に関するレコードのステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-191"><strong>Record</strong> オブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-193"><strong>Resync</strong> の呼び出しによって、基になる値が上書きされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="09eef-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-p103"><strong>Stream</strong> オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="09eef-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-198"><strong>OpenSchema</strong> メソッドが取得するスキーマ <strong>Recordset</strong> の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-198">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves.</span></span> <span data-ttu-id="09eef-199"><strong>Recordset</strong> 内のレコードの検索方向を表します。</span><span class="sxs-lookup"><span data-stu-id="09eef-199">Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-201"><strong>Recordset</strong>内でのレコード検索の方向を指定します。実行する<strong>Seek</strong>の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-203">実行する<strong>Seek</strong>の種類を指定します。<strong>Stream</strong>オブジェクトを開くときのオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-203">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="09eef-204">これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="09eef-204">The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-206"><strong>Stream</strong> オブジェクトを開くときのオプションを表します。</span><span class="sxs-lookup"><span data-stu-id="09eef-206">Specifies options for opening a <strong>Stream</strong> object.</span></span> <span data-ttu-id="09eef-207">これらの値は、and 演算子と組み合わせて使用できます。stream オブジェクトから、ストリーム全体を読み取るか、または次の<strong></strong>行を読み取るかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-207">The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-209">stream オブジェクトから、ストリーム全体を読み取るか、または次の<strong></strong>行を読み取るかを指定します。<strong>Stream</strong>オブジェクトに格納されているデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-211"><strong>Stream</strong>オブジェクトに格納されているデータの種類を指定します。<strong>Stream</strong>オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-213"><strong>Stream</strong>オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを指定します。文字列として<strong>Recordset</strong>を取得するときの形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eef-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-215">文字列として<strong>Recordset</strong>を取得するときの形式を指定します。<strong>Connection</strong>オブジェクトのトランザクション属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="09eef-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eef-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="09eef-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="09eef-217"><strong>Connection</strong> オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="09eef-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

