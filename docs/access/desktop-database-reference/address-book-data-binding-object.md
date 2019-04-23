---
title: アドレス帳のデータバインディング オブジェクト
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fb5302d1c2b8e4eebb6dbe1a5906459834b8e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281868"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="bc6fc-102">アドレス帳のデータバインディング オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bc6fc-102">Address Book Data-Binding object</span></span>


<span data-ttu-id="bc6fc-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc6fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc6fc-p101">Address Book アプリケーションでは、[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを使って、SQL Server データベースのデータをクライアントの HTML ページに表示されるオブジェクト (この場合は DHTML テーブル) にバインドします。イベントドリブン型の VBScript プログラム ロジックでは、 [RDS.DataControl](datacontrol-object-rds.md) を使って次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-p101">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page. The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="bc6fc-106">データベースのクエリ、データベースへの更新の送信、およびデータ グリッドの更新を行います。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="bc6fc-107">ユーザーがデータ グリッド内の最初のレコード、最後のレコード、または現在のレコードの前後のレコードに移動できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="bc6fc-108">次のコードで、 **RDS.DataControl** コンポーネントを定義します。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="bc6fc-p102">OBJECT タグで、 **RDS.DataControl** コンポーネントをプログラム内に定義します。このタグには、次の 2 種類のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-p102">The OBJECT tag defines the **RDS.DataControl** component in the program. The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="bc6fc-111">一般的な OBJECT タグに関連するパラメーター</span><span class="sxs-lookup"><span data-stu-id="bc6fc-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="bc6fc-112">**RDS.DataControl** オブジェクトに固有のパラメーター</span><span class="sxs-lookup"><span data-stu-id="bc6fc-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="bc6fc-113">一般的な OBJECT タグ パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc6fc-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="bc6fc-114">次の表に、OBJECT タグに関連するパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc6fc-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc6fc-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="bc6fc-116">説明</span><span class="sxs-lookup"><span data-stu-id="bc6fc-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc6fc-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="bc6fc-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="bc6fc-p103">一意の 128 ビットの数字で、システムの埋め込みオブジェクトの種類を識別します。この識別子は、ローカル コンピューターのシステム レジストリに保持されます (<strong>RDS.DataControl</strong> オブジェクトのクラス ID については、「<a href="datacontrol-object-rds.md">DataControl オブジェクト (RDS)</a>」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-p103">A unique, 128-bit number that identifies the type of embedded object to the system. This identifier is maintained in the local computer's system registry. (For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc6fc-121"><strong><em>ID</em></strong></span><span class="sxs-lookup"><span data-stu-id="bc6fc-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="bc6fc-122">埋め込みオブジェクトの、ドキュメント全体での識別子であり、コード内でオブジェクトを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="bc6fc-123">RDS.DataControl タグ パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc6fc-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="bc6fc-p104">次の表に、**RDS.DataControl** オブジェクトに固有のパラメーターを示します。**RDS.DataControl** オブジェクトのすべてのパラメーター一覧、およびその実装時期については、「[DataControl オブジェクト (RDS)](datacontrol-object-rds.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-p104">The following table describes the parameters specific to the **RDS.DataControl** object. (For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc6fc-126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc6fc-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="bc6fc-127">説明</span><span class="sxs-lookup"><span data-stu-id="bc6fc-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc6fc-128"><a href="server-property-rds.md">SERVER</a></span><span class="sxs-lookup"><span data-stu-id="bc6fc-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="bc6fc-129">HTTP を使用している場合、値はサーバーコンピューターの名前で、その後に https://が付加されます。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc6fc-130"><a href="connect-property-rds.md">結び付ける</a></span><span class="sxs-lookup"><span data-stu-id="bc6fc-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="bc6fc-131">SQL Server に接続するために <strong>RDS.DataControl</strong> に必要な接続情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc6fc-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span><span class="sxs-lookup"><span data-stu-id="bc6fc-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="bc6fc-133"><a href="recordset-object-ado.md">Recordset</a> を取得するために使用されるクエリ文字列を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="bc6fc-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

