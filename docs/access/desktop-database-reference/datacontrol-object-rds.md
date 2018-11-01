---
title: DataControl オブジェクト (RDS)
TOCTitle: DataControl Object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1735de700fe1b0e786f55f0539495656dd9db2d7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883002"
---
# <a name="datacontrol-object-rds"></a><span data-ttu-id="04b34-102">DataControl オブジェクト (RDS)</span><span class="sxs-lookup"><span data-stu-id="04b34-102">DataControl Object (RDS)</span></span>

<span data-ttu-id="04b34-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="04b34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04b34-104">1 つまたは複数のコントロール (たとえば、テキスト ボックス、グリッド コントロール、またはコンボ ボックス) web ページの**レコード セット**データを表示するには、データ クエリ[のレコード セット](recordset-object-ado.md)をバインドします。</span><span class="sxs-lookup"><span data-stu-id="04b34-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b34-105">構文</span><span class="sxs-lookup"><span data-stu-id="04b34-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="04b34-106">備考</span><span class="sxs-lookup"><span data-stu-id="04b34-106">Remarks</span></span>

<span data-ttu-id="04b34-107">**RDS.DataControl** オブジェクトのクラス ID は、BD96C556-65A3-11D0-983A-00C04FC29E33 です。</span><span class="sxs-lookup"><span data-stu-id="04b34-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="04b34-p101">[!メモ] [RDS.DataSpace](dataspace-object-rds.md) オブジェクトまたは **RDS.DataControl** オブジェクトを読み込むことができないというエラーが発生した場合は、正しいクラス ID を使用していることを確認してください。これらのオブジェクトのクラス ID は、バージョン 1.0 とバージョン 1.1 から変更されています。</span><span class="sxs-lookup"><span data-stu-id="04b34-p101">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID. The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="04b34-110">基本的なシナリオでは、既定のビジネス オブジェクトの **RDSServer.DataFactory** を自動的に呼び出す、 **RDS.DataControl** オブジェクトの **SQL** 、 **Connect** 、および [Server](datafactory-object-rdsserver.md) の各プロパティのみ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b34-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="04b34-111">**RDS.DataControl** のすべてのプロパティは、カスタムのビジネス オブジェクトでその機能を置き換えられるため省略可能です。</span><span class="sxs-lookup"><span data-stu-id="04b34-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="04b34-112">[!メモ] 複数の結果を求めるクエリを実行すると、最初の [Recordset](recordset-object-ado.md) のみ取得されます。</span><span class="sxs-lookup"><span data-stu-id="04b34-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="04b34-113">複数の結果セットが必要な場合は、それぞれを独自の **DataControl** に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="04b34-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="04b34-114">複数の結果のクエリの例は以下である可能性があります: `"Select * from Authors, Select * from Topics"`。</span><span class="sxs-lookup"><span data-stu-id="04b34-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="04b34-p103">**RDS.DataControl** オブジェクトを使用する場合、接続文字列に "DFMode=20;" を追加すると、データ更新時のサーバーのパフォーマンスを向上させることができます。この設定によって、サーバー上の **RDSServer.DataFactory** オブジェクトはリソース消費量の少ないモードを使用します。ただし、この設定では次の機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="04b34-p103">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data. With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode. However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="04b34-118">パラメーター クエリを使用する。</span><span class="sxs-lookup"><span data-stu-id="04b34-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="04b34-119">**Execute** メソッドを呼び出す前に、パラメーターまたは列の情報を取得する。</span><span class="sxs-lookup"><span data-stu-id="04b34-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="04b34-120">**Transact Updates** を **True** に設定する。</span><span class="sxs-lookup"><span data-stu-id="04b34-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="04b34-121">行のステータスを取得する。</span><span class="sxs-lookup"><span data-stu-id="04b34-121">Getting row status.</span></span>

  - <span data-ttu-id="04b34-122">[Resync](resync-method-ado.md) メソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="04b34-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="04b34-123">[Update Resync](update-resync-property-dynamic-ado.md) プロパティによって明示的または自動的に更新する。</span><span class="sxs-lookup"><span data-stu-id="04b34-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="04b34-124">**Command** プロパティまたは [Recordset](recordset-sourcerecordset-properties-rds.md) プロパティを設定する。</span><span class="sxs-lookup"><span data-stu-id="04b34-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="04b34-125">**adCmdTableDirect** を使用する。</span><span class="sxs-lookup"><span data-stu-id="04b34-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="04b34-p104">**RDS.DataControl** オブジェクトは、既定では非同期モードで実行されます。アプリケーションを同期モードで実行する必要がある場合は、次の例で示すように、 [ExecuteOptions](executeoptions-property-rds.md) パラメーターを **adcExecSync** と同じ値に、 [FetchOptions](fetchoptions-property-rds.md) パラメーターを **adcFetchUpFront** と同じ値に設定します。</span><span class="sxs-lookup"><span data-stu-id="04b34-p104">The **RDS.DataControl** object runs in asynchronous mode by default. If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

<span data-ttu-id="04b34-p105">単一のクエリの結果を 1 つまたは複数のビジュアル コントロールにリンクするには、1 つの **RDS.DataControl** オブジェクトを使用します。たとえば、名前、住居、出生地、年齢、優先得意先ステータスなどの顧客データを要求するクエリのコードを作成するとします。この場合、1 つの **RDS.DataControl** オブジェクトを使用して、顧客の名前、年齢、地域を 3 つの異なるテキスト ボックスに、優先顧客ステータスを 1 つのチェック ボックスに、すべてのデータをグリッド コントロールに表示できます。</span><span class="sxs-lookup"><span data-stu-id="04b34-p105">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls. For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status. You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="04b34-p106">複数のクエリの結果を異なるビジュアル コントロールにリンクするには、異なる **RDS.DataControl** オブジェクトを使用します。たとえば、1 つ目のクエリを使用して得意先に関する情報を取得し、2 つ目のクエリを使用して得意先が購入した商品に関する情報を取得するとします。最初のクエリの結果を 3 つのテキスト ボックスと 1 つのチェック ボックスに、2 つ目のクエリの結果をグリッド コントロールに表示します。既定のビジネス オブジェクト (**RDSServer.DataFactory**) を使用する場合、次のような操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b34-p106">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls. For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased. You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control. If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="04b34-135">2 つの追加**rds.DataControl**オブジェクトを web ページにします。</span><span class="sxs-lookup"><span data-stu-id="04b34-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="04b34-p107">2 つの **RDS.DataControl** オブジェクトの各 **SQL** プロパティに 1 つずつ、合計 2 つのクエリを記述します。1 つ目の **RDS.DataControl** オブジェクトには、顧客の情報を要求する SQL クエリを、2 つ目のオブジェクトには、顧客が購入した商品の一覧を要求するクエリを格納します。</span><span class="sxs-lookup"><span data-stu-id="04b34-p107">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="04b34-138">連結コントロールの各 OBJECT タグで、DATAFLD 値を指定して、各ビジュアル コントロールに表示するデータの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="04b34-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="04b34-139">**Rds. 数のカウントの制限はありません。DataControl**オブジェクトを 1 つの web ページ上のオブジェクト タグを使用して埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="04b34-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="04b34-140">Rds. の**を定義する場合DataControl** web ページ上のオブジェクト、1、0 以外の**幅**と**高さ**の値を使用して、避けるために余分なスペースを含めること)。</span><span class="sxs-lookup"><span data-stu-id="04b34-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="04b34-141">リモート データ サービスのクライアント コンポーネントは、Internet Explorer 4.0 の一部として既に組み込まれています。このため、 **RDS.DataControl** オブジェクトのタグに、CODEBASE パラメーターを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="04b34-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="04b34-142">Internet Explorer 4.0 以降では、HTML コントロールと ActiveX® コントロールがアパートメント モデル コントロールに設定されている場合にのみ、これらのコントロールを使用してデータに連結できます。</span><span class="sxs-lookup"><span data-stu-id="04b34-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX® controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="04b34-143">**Microsoft Visual Basic のユーザー\*\*\*\*Rds.DataControl** 、web ベースのアプリケーションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="04b34-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="04b34-144">Visual Basic クライアント アプリケーションでは不要です。</span><span class="sxs-lookup"><span data-stu-id="04b34-144">A Visual Basic client application has no need for it.</span></span>

